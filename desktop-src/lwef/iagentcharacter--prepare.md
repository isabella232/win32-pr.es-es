---
title: Preparación de IAgentCharacter
description: Preparación de IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119880"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="71d1f-103">IAgentCharacter::P repare</span><span class="sxs-lookup"><span data-stu-id="71d1f-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="71d1f-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71d1f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="71d1f-105">Recupera los datos de animación de un carácter.</span><span class="sxs-lookup"><span data-stu-id="71d1f-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="71d1f-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="71d1f-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="71d1f-107">Cuando la función devuelve un resultado, *pdwReqID* contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71d1f-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="71d1f-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="71d1f-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="71d1f-109">Valor que indica el tipo de datos de animación que se va a cargar y que debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="71d1f-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="71d1f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="71d1f-110">Value</span></span>                                                           | <span data-ttu-id="71d1f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="71d1f-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="71d1f-112">**const unsigned short** **PREPARE ANIMATION = \_ 0;**</span><span class="sxs-lookup"><span data-stu-id="71d1f-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="71d1f-113">Datos de animación de un carácter.</span><span class="sxs-lookup"><span data-stu-id="71d1f-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="71d1f-114">**const unsigned short** **PREPARE STATE = \_ 1;**</span><span class="sxs-lookup"><span data-stu-id="71d1f-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="71d1f-115">Datos de estado de un carácter.</span><span class="sxs-lookup"><span data-stu-id="71d1f-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="71d1f-116">**const unsigned short** **PREPARE WAVE = \_ 2**</span><span class="sxs-lookup"><span data-stu-id="71d1f-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="71d1f-117">Archivo de sonido de un carácter (. WAV o . LWV) para la salida hablada.</span><span class="sxs-lookup"><span data-stu-id="71d1f-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="71d1f-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="71d1f-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="71d1f-119">Nombre de la animación o el estado.</span><span class="sxs-lookup"><span data-stu-id="71d1f-119">The name of the animation or state.</span></span>

<span data-ttu-id="71d1f-120">El nombre de animación se basa en el definido para el carácter cuando se guardó mediante el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="71d1f-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="71d1f-121">Para los estados, el valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="71d1f-121">For states, the value can be one of the following:</span></span>



|                      | <span data-ttu-id="71d1f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="71d1f-122">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="71d1f-123">**"Gesturing"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-123">**"Gesturing"**</span></span>      | <span data-ttu-id="71d1f-124">Para recuperar todas las **animaciones de estado Gesturing.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-124">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="71d1f-125">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-125">**"GesturingDown"**</span></span>  | <span data-ttu-id="71d1f-126">Para recuperar **animaciones GesturingDown.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-126">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="71d1f-127">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-127">**"GesturingLeft"**</span></span>  | <span data-ttu-id="71d1f-128">Para recuperar **animaciones GesturingLeft.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-128">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="71d1f-129">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-129">**"GesturingRight"**</span></span> | <span data-ttu-id="71d1f-130">Para recuperar **animaciones GesturingRight.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-130">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="71d1f-131">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-131">**"GesturingUp"**</span></span>    | <span data-ttu-id="71d1f-132">Para recuperar **animaciones GesturingUp.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-132">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="71d1f-133">**"Ocultar"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-133">**"Hiding"**</span></span>         | <span data-ttu-id="71d1f-134">Para recuperar las **animaciones de** estado Ocultar.</span><span class="sxs-lookup"><span data-stu-id="71d1f-134">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="71d1f-135">**"Audiencia"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-135">**"Hearing"**</span></span>        | <span data-ttu-id="71d1f-136">Para recuperar las **animaciones de** estado de la audiencia.</span><span class="sxs-lookup"><span data-stu-id="71d1f-136">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="71d1f-137">**"Idling"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-137">**"Idling"**</span></span>         | <span data-ttu-id="71d1f-138">Para recuperar todas las animaciones de estado de **idling.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-138">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="71d1f-139">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-139">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="71d1f-140">Para recuperar todas **las animaciones IdlingLevel1.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-140">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="71d1f-141">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-141">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="71d1f-142">Para recuperar todas **las animaciones IdlingLevel2.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-142">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="71d1f-143">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-143">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="71d1f-144">Para recuperar todas **las animaciones IdlingLevel3.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-144">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="71d1f-145">**"Escuchando"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-145">**"Listening"**</span></span>      | <span data-ttu-id="71d1f-146">Para recuperar las **animaciones de** estado De escucha.</span><span class="sxs-lookup"><span data-stu-id="71d1f-146">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="71d1f-147">**"Mover"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-147">**"Moving"**</span></span>         | <span data-ttu-id="71d1f-148">Para recuperar todas las **animaciones de** estado de movimiento.</span><span class="sxs-lookup"><span data-stu-id="71d1f-148">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="71d1f-149">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-149">**"MovingDown"**</span></span>     | <span data-ttu-id="71d1f-150">Para recuperar todas **las animaciones de** movimiento.</span><span class="sxs-lookup"><span data-stu-id="71d1f-150">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="71d1f-151">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-151">**"MovingLeft"**</span></span>     | <span data-ttu-id="71d1f-152">Para recuperar todas **las animaciones MovingLeft.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-152">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="71d1f-153">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-153">**"MovingRight"**</span></span>    | <span data-ttu-id="71d1f-154">Para recuperar todas **las animaciones MovingRight.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-154">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="71d1f-155">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-155">**"MovingUp"**</span></span>       | <span data-ttu-id="71d1f-156">Para recuperar todas **las animaciones MovingUp.**</span><span class="sxs-lookup"><span data-stu-id="71d1f-156">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="71d1f-157">**"Mostrando"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-157">**"Showing"**</span></span>        | <span data-ttu-id="71d1f-158">Para recuperar las **animaciones de** estado Mostrando.</span><span class="sxs-lookup"><span data-stu-id="71d1f-158">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="71d1f-159">**"Habla"**</span><span class="sxs-lookup"><span data-stu-id="71d1f-159">**"Speaking"**</span></span>       | <span data-ttu-id="71d1f-160">Para recuperar las **animaciones de** estado de habla.</span><span class="sxs-lookup"><span data-stu-id="71d1f-160">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="71d1f-161">Para. Archivos WAV, establezca *bszName en* la dirección URL o la especificación de archivo para . Archivo WAV.</span><span class="sxs-lookup"><span data-stu-id="71d1f-161">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="71d1f-162">Si la especificación no está completa, se interpreta como relativa a la especificación usada en el [**método Load.**](https://www.bing.com/search?q=**Load**)</span><span class="sxs-lookup"><span data-stu-id="71d1f-162">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="71d1f-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="71d1f-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="71d1f-164">Valor booleano que especifica si el servidor pone en cola la [**solicitud Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare)</span><span class="sxs-lookup"><span data-stu-id="71d1f-164">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="71d1f-165">**True** pone en cola la solicitud y hace que cualquier solicitud de animación que le sigue espere hasta que se carguen los datos de animación que especifica.</span><span class="sxs-lookup"><span data-stu-id="71d1f-165">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="71d1f-166">**False** recupera los datos de animación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="71d1f-166">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="71d1f-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="71d1f-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="71d1f-168">Dirección de una variable que recibe el identificador [**de solicitud**](/windows/desktop/lwef/iagentcharacter--prepare) de preparación.</span><span class="sxs-lookup"><span data-stu-id="71d1f-168">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="71d1f-169">Si carga un carácter mediante el protocolo HTTP (un . Archivo ACF), debe usar el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para recuperar datos de animación antes de poder reproducir la animación.</span><span class="sxs-lookup"><span data-stu-id="71d1f-169">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="71d1f-170">No puede usar este método si cargó el carácter mediante el protocolo UNC (un . ARCHIVO DE ACS).</span><span class="sxs-lookup"><span data-stu-id="71d1f-170">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="71d1f-171">Tampoco puede recuperar datos HTTP para un carácter mediante **Prepare** si cargó ese carácter mediante el protocolo UNC (. Archivo de caracteres de ACS).</span><span class="sxs-lookup"><span data-stu-id="71d1f-171">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="71d1f-172">Los datos de animación o sonido recuperados con [**el método Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) se almacenan en la memoria caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="71d1f-172">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="71d1f-173">Las llamadas posteriores comprobarán la memoria caché y, si los datos de animación ya están allí, el control carga los datos directamente desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="71d1f-173">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="71d1f-174">Una vez cargados, los datos de animación o sonido se pueden reproducir con los [**métodos Play**](/windows/desktop/lwef/iagentcharacter--play) [**o Speak.**](/windows/desktop/lwef/iagentcharacter--speak)</span><span class="sxs-lookup"><span data-stu-id="71d1f-174">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="71d1f-175">Puede especificar varias animaciones y estados si los separa con comas.</span><span class="sxs-lookup"><span data-stu-id="71d1f-175">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="71d1f-176">Sin embargo, no puede mezclar tipos en la misma [**instrucción Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare)</span><span class="sxs-lookup"><span data-stu-id="71d1f-176">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

