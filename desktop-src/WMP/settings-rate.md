---
title: Settings. rate
description: La propiedad Rate especifica o recupera la velocidad de reproducción actual de los medios de vídeo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Configuración. rate Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653573"
---
# <a name="settingsrate"></a><span data-ttu-id="9861b-104">Settings. rate</span><span class="sxs-lookup"><span data-stu-id="9861b-104">Settings.rate</span></span>

<span data-ttu-id="9861b-105">La propiedad **Rate** especifica o recupera la velocidad de reproducción actual de los medios de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9861b-105">The **rate** property specifies or retrieves the current playback rate of video media.</span></span>

## <a name="syntax"></a><span data-ttu-id="9861b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9861b-106">Syntax</span></span>

<span data-ttu-id="9861b-107">Player. Settings. rate</span><span class="sxs-lookup"><span data-stu-id="9861b-107">player.settings.rate</span></span>

## <a name="possible-values"></a><span data-ttu-id="9861b-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="9861b-108">Possible Values</span></span>

<span data-ttu-id="9861b-109">Esta propiedad es un **número** de lectura/escritura (**Double**) con un valor predeterminado de 1,0.</span><span class="sxs-lookup"><span data-stu-id="9861b-109">This property is a read/write **Number** (**double**) with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="9861b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9861b-110">Remarks</span></span>

<span data-ttu-id="9861b-111">Esta propiedad actúa como un valor de multiplicador que permite reproducir un clip a una velocidad mayor o menor.</span><span class="sxs-lookup"><span data-stu-id="9861b-111">This property acts as a multiplier value that allows you to play a clip at a faster or slower rate.</span></span> <span data-ttu-id="9861b-112">El valor predeterminado de 1,0 indica la velocidad de creación.</span><span class="sxs-lookup"><span data-stu-id="9861b-112">The default value of 1.0 indicates the authored speed.</span></span> <span data-ttu-id="9861b-113">Tenga en cuenta que una pista de audio es difícil de comprender a las tarifas inferiores a 0,5 o superior a 1,5.</span><span class="sxs-lookup"><span data-stu-id="9861b-113">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="9861b-114">Una velocidad de reproducción de 2 equivale a dos veces la velocidad de reproducción normal.</span><span class="sxs-lookup"><span data-stu-id="9861b-114">A playback rate of 2 equates to twice the normal playback speed.</span></span>

<span data-ttu-id="9861b-115">Windows Media Player intentará usar los cuatro modos de reproducción más efectivos.</span><span class="sxs-lookup"><span data-stu-id="9861b-115">Windows Media Player will attempt to use the most effective of four different playback modes.</span></span> <span data-ttu-id="9861b-116">Estos modos son la reproducción de vídeo sin problemas con el paso de audio, la reproducción fluida de vídeo con el tono de audio no mantenido, la reproducción de vídeo suave sin audio y la reproducción de vídeo de fotogramas clave sin audio.</span><span class="sxs-lookup"><span data-stu-id="9861b-116">These modes are smooth video playback with audio pitch maintained, smooth video playback with audio pitch not maintained, smooth video playback with no audio, and keyframe video playback with no audio.</span></span> <span data-ttu-id="9861b-117">El modo elegido por el reproductor depende de numerosos factores, como el tipo de archivo y la ubicación, el sistema operativo, la red y el servidor.</span><span class="sxs-lookup"><span data-stu-id="9861b-117">The mode chosen by the Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="9861b-118">También se aplican otras consideraciones, según el tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="9861b-118">Other considerations apply as well, depending on media type:</span></span>

-   <span data-ttu-id="9861b-119">Windows Media Format (WMV) y archivos ASF: los valores óptimos para esta propiedad son de 1 a 10, o de 1 a 10 para la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="9861b-119">Windows Media Format (WMV) and ASF files: Optimal values for this property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="9861b-120">Los valores de 0,5 a 1,0 o de-0,5 a-1,0 también pueden funcionar bien en los casos en los que se pueda mantener el tono de audio, por ejemplo, al reproducir archivos ubicados en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9861b-120">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, for example, when playing files located on the local computer.</span></span> <span data-ttu-id="9861b-121">Se permiten los valores con una magnitud absoluta mayor que 10, pero no son muy significativos.</span><span class="sxs-lookup"><span data-stu-id="9861b-121">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="9861b-122">Otros tipos de medios de vídeo: esta propiedad puede oscilar entre 0 y 9.</span><span class="sxs-lookup"><span data-stu-id="9861b-122">Other Video Media Types: This property can range from 0 to 9.</span></span> <span data-ttu-id="9861b-123">No se permiten valores negativos.</span><span class="sxs-lookup"><span data-stu-id="9861b-123">Negative values are not allowed.</span></span> <span data-ttu-id="9861b-124">Los valores menores que 1 representan un movimiento lento.</span><span class="sxs-lookup"><span data-stu-id="9861b-124">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="9861b-125">Los valores por encima de 9 están permitidos, pero no son muy significativos.</span><span class="sxs-lookup"><span data-stu-id="9861b-125">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="9861b-126">*Controles*. el método **fastForward** cambia el valor de **Rate** a 5,0, mientras que los *controles*. el método **fastReverse** cambia la **velocidad** a 5,0.</span><span class="sxs-lookup"><span data-stu-id="9861b-126">The *Controls*.**fastForward** method changes the value of **rate** to 5.0, while the *Controls*.**fastReverse** method changes **rate** to  5.0.</span></span>

<span data-ttu-id="9861b-127">No se puede modificar la velocidad de reproducción de algunos tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="9861b-127">The playback rate of some media types cannot be altered.</span></span> <span data-ttu-id="9861b-128">Utilice la *configuración*. método **isavailable** para determinar si esta propiedad se puede especificar para un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="9861b-128">Use the *Settings*.**isAvailable** method to determine whether this property can be specified for a particular media item.</span></span>

<span data-ttu-id="9861b-129">**Windows Media Player 10 Mobile**: esta propiedad solo acepta o devuelve valores de-5,0, 1,0 o 5,0.</span><span class="sxs-lookup"><span data-stu-id="9861b-129">**Windows Media Player 10 Mobile**: This property only accepts or returns values of -5.0, 1.0, or 5.0.</span></span>

## <a name="examples"></a><span data-ttu-id="9861b-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9861b-130">Examples</span></span>

<span data-ttu-id="9861b-131">En el ejemplo siguiente se crea un elemento SELECT de HTML que permite al usuario cambiar la velocidad de reproducción del medio actual.</span><span class="sxs-lookup"><span data-stu-id="9861b-131">The following example creates an HTML SELECT element that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="9861b-132">Las opciones SELECT ofrecen velocidades normales, velocidad media y velocidad de reproducción de velocidad doble.</span><span class="sxs-lookup"><span data-stu-id="9861b-132">The SELECT options offer normal speed, half -speed and double-speed playback rates.</span></span> <span data-ttu-id="9861b-133">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9861b-133">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="9861b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9861b-134">Requirements</span></span>



| <span data-ttu-id="9861b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9861b-135">Requirement</span></span> | <span data-ttu-id="9861b-136">Value</span><span class="sxs-lookup"><span data-stu-id="9861b-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9861b-137">Versión</span><span class="sxs-lookup"><span data-stu-id="9861b-137">Version</span></span><br/> | <span data-ttu-id="9861b-138">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9861b-138">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9861b-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9861b-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="9861b-140"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9861b-140"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9861b-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9861b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9861b-142">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="9861b-142">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="9861b-143">**Controls. fastReverse**</span><span class="sxs-lookup"><span data-stu-id="9861b-143">**Controls.fastReverse**</span></span>](controls-fastreverse.md)
</dt> <dt>

[<span data-ttu-id="9861b-144">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="9861b-144">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="9861b-145">**Settings. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="9861b-145">**Settings.isAvailable**</span></span>](settings-isavailable.md)
</dt> </dl>

 

 





