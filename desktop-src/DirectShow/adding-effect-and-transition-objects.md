---
description: Agregar objetos Effect y Transition
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Agregar objetos Effect y Transition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079956"
---
# <a name="adding-effect-and-transition-objects"></a><span data-ttu-id="fdc11-103">Agregar objetos Effect y Transition</span><span class="sxs-lookup"><span data-stu-id="fdc11-103">Adding Effect and Transition Objects</span></span>

<span data-ttu-id="fdc11-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="fdc11-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="fdc11-105">En DES, un efecto o una transición se representa con dos objetos:</span><span class="sxs-lookup"><span data-stu-id="fdc11-105">In DES, an effect or transition is represented with two objects:</span></span>

-   <span data-ttu-id="fdc11-106">Un *objeto Timeline* representa el efecto o la transición dentro de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fdc11-106">A *timeline object* represents the effect or transition within the timeline.</span></span> <span data-ttu-id="fdc11-107">En el caso de los efectos, el objeto Timeline admite la interfaz [**IAMTimelineEffect**](iamtimelineeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="fdc11-107">For effects, the timeline object supports the [**IAMTimelineEffect**](iamtimelineeffect.md) interface.</span></span> <span data-ttu-id="fdc11-108">En el caso de las transiciones, admite la interfaz [**IAMTimelineTrans**](iamtimelinetrans.md) .</span><span class="sxs-lookup"><span data-stu-id="fdc11-108">For transitions, it supports the [**IAMTimelineTrans**](iamtimelinetrans.md) interface.</span></span> <span data-ttu-id="fdc11-109">Ambos tipos admiten la interfaz [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="fdc11-109">Both types support the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>
-   <span data-ttu-id="fdc11-110">El *subobjeto* es un objeto que implementa el procesamiento de datos para el efecto o la transición.</span><span class="sxs-lookup"><span data-stu-id="fdc11-110">The *subobject* is an object that implements the data processing for the effect or transition.</span></span> <span data-ttu-id="fdc11-111">El objeto Timeline contiene un puntero al subobjeto.</span><span class="sxs-lookup"><span data-stu-id="fdc11-111">The timeline object holds a pointer to the subobject.</span></span>

<span data-ttu-id="fdc11-112">Para agregar un efecto o una transición, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="fdc11-112">To add an effect or transition, perform the following steps.</span></span>

<span data-ttu-id="fdc11-113">**1. crear el objeto Timeline**</span><span class="sxs-lookup"><span data-stu-id="fdc11-113">**1. Create the Timeline Object**</span></span>

<span data-ttu-id="fdc11-114">Para crear el objeto Timeline, llame al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="fdc11-114">To create the timeline object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="fdc11-115">Establezca el tipo igual a la **escala de tiempo del \_ \_ \_ efecto de tipo principal** para un efecto o la **\_ \_ \_ transición de tipo principal** de la escala de tiempo para una transición.</span><span class="sxs-lookup"><span data-stu-id="fdc11-115">Set the type equal to **TIMELINE\_MAJOR\_TYPE\_EFFECT** for an effect, or **TIMELINE\_MAJOR\_TYPE\_TRANSITION** for a transition.</span></span>

<span data-ttu-id="fdc11-116">En el ejemplo siguiente se crea un objeto de transición:</span><span class="sxs-lookup"><span data-stu-id="fdc11-116">The following example creates a transition object:</span></span>


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



<span data-ttu-id="fdc11-117">**2. especificar el subobjeto**</span><span class="sxs-lookup"><span data-stu-id="fdc11-117">**2. Specify the Subobject**</span></span>

<span data-ttu-id="fdc11-118">El objeto Timeline actúa como contenedor de otro objeto, denominado *subobjeto*, que realiza el trabajo real.</span><span class="sxs-lookup"><span data-stu-id="fdc11-118">The timeline object acts as a wrapper for another object, called the *subobject*, which does the real work.</span></span> <span data-ttu-id="fdc11-119">El subobjeto implementa una transformación de datos que produce el efecto o la transición deseados.</span><span class="sxs-lookup"><span data-stu-id="fdc11-119">The subobject implements a data transform that produces the desired effect or transition.</span></span> <span data-ttu-id="fdc11-120">Para obtener una lista de las transiciones y los efectos proporcionados con DES, consulte [transiciones y efectos](transitions-and-effects.md).</span><span class="sxs-lookup"><span data-stu-id="fdc11-120">For a list of transitions and effects supplied with DES, see [Transitions and Effects](transitions-and-effects.md).</span></span>

<span data-ttu-id="fdc11-121">Para establecer el subobjeto, llame al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) en el objeto Timeline, pasándole el identificador de clase (CLSID) del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="fdc11-121">To set the subobject, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method on the timeline object, passing it the class identifier (CLSID) of the subobject.</span></span> <span data-ttu-id="fdc11-122">DirectShow proporciona un enumerador para los efectos de vídeo y las transiciones de vídeo, que puede usar para obtener el CLSID.</span><span class="sxs-lookup"><span data-stu-id="fdc11-122">DirectShow provides an enumerator for video effects and video transitions, which you can use to obtain the CLSID.</span></span> <span data-ttu-id="fdc11-123">Para obtener más información, consulte [enumeración de efectos y transiciones](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="fdc11-123">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="fdc11-124">En el ejemplo siguiente se establece la [transición de borrado de SMPTE](smpte-wipe-transition.md) como el subobjeto:</span><span class="sxs-lookup"><span data-stu-id="fdc11-124">The following example sets the [SMPTE Wipe Transition](smpte-wipe-transition.md) as the subobject :</span></span>


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



<span data-ttu-id="fdc11-125">**3. establecer las horas de inicio y detención**</span><span class="sxs-lookup"><span data-stu-id="fdc11-125">**3. Set the Start and Stop Times**</span></span>

<span data-ttu-id="fdc11-126">Para establecer las horas de inicio y detención, llame al método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="fdc11-126">To set the start and stop times, call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="fdc11-127">Estas horas son relativas a la hora de inicio del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="fdc11-127">These times are relative to the start time of the parent object.</span></span> <span data-ttu-id="fdc11-128">Los efectos pueden superponerse dentro del mismo objeto, pero las transiciones no.</span><span class="sxs-lookup"><span data-stu-id="fdc11-128">Effects can overlap within the same object, but transitions cannot.</span></span>

<span data-ttu-id="fdc11-129">En el ejemplo siguiente se establece la hora de inicio en 5 segundos y la hora de detención en 10 segundos:</span><span class="sxs-lookup"><span data-stu-id="fdc11-129">The following example sets the start time to 5 seconds and the stop time to 10 seconds:</span></span>


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



<span data-ttu-id="fdc11-130">Cuando se representa una transición, el progreso de la transición en cada fotograma se calcula en función de una propiedad de **progreso** , que se normaliza en un intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="fdc11-130">When a transition is rendered, the progress of the transition at each frame is calculated based on a **Progress** property, which is normalized to a range of 0.0 to 1.0.</span></span> <span data-ttu-id="fdc11-131">DES usa la hora de inicio de cada fotograma para calcular el valor de progreso.</span><span class="sxs-lookup"><span data-stu-id="fdc11-131">DES uses the start time of each frame to calculate the progress value.</span></span> <span data-ttu-id="fdc11-132">Esto significa que si la hora de detención de la transición es igual a la hora de detención del origen, el valor de **progreso** nunca alcanzará exactamente 1,0, porque la hora de inicio del último fotograma es ligeramente menor que la hora de detención.</span><span class="sxs-lookup"><span data-stu-id="fdc11-132">This means if the transition stop time is equal to the source stop time, the **Progress** value will never reach exactly 1.0, because the start time of the last frame is slightly than the stop time.</span></span> <span data-ttu-id="fdc11-133">Para que la transición llegue a 1,0, establezca la hora de detención de la transición para que sea al menos un fotograma anterior a la hora de detención del origen.</span><span class="sxs-lookup"><span data-stu-id="fdc11-133">To make the transition reach 1.0, set the transition stop time to be at least one frame earlier than the source stop time.</span></span>

<span data-ttu-id="fdc11-134">**4. Insertar el objeto en la escala de tiempo**</span><span class="sxs-lookup"><span data-stu-id="fdc11-134">**4. Insert the Object into the Timeline**</span></span>

<span data-ttu-id="fdc11-135">Para insertar el objeto en la escala de tiempo, llame a uno de los métodos siguientes en el elemento primario, en función del tipo de objeto:</span><span class="sxs-lookup"><span data-stu-id="fdc11-135">To insert the object into the timeline, call one of the following methods on the parent, depending on the object type:</span></span>

-   <span data-ttu-id="fdc11-136">Efectos: [ **IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span><span class="sxs-lookup"><span data-stu-id="fdc11-136">Effects: [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span></span>
-   <span data-ttu-id="fdc11-137">Transiciones: [ **IAMTimelineTransable:: TransAdd**](iamtimelinetransable-transadd.md)</span><span class="sxs-lookup"><span data-stu-id="fdc11-137">Transitions: [**IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)</span></span>

<span data-ttu-id="fdc11-138">En el método [**IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) , debe especificar la prioridad del efecto.</span><span class="sxs-lookup"><span data-stu-id="fdc11-138">In the [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) method, you must specify the priority of the effect.</span></span> <span data-ttu-id="fdc11-139">Cuando los efectos se superponen en el mismo objeto, se aplican en orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="fdc11-139">When effects overlap on the same object, they are applied in order of priority.</span></span> <span data-ttu-id="fdc11-140">El efecto de audio de sobre de volumen es una excepción; Consulte la referencia de [efectos de sobre de volumen](volume-envelope-effect.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="fdc11-140">The Volume Envelope audio effect is an exception; see the [Volume Envelope Effect](volume-envelope-effect.md) reference for details.</span></span> <span data-ttu-id="fdc11-141">Dentro de una composición, todas las pistas de audio se mezclan antes de que se apliquen los efectos de audio de la composición.</span><span class="sxs-lookup"><span data-stu-id="fdc11-141">Within a composition, all audio tracks are mixed before the audio effects for that composition are applied.</span></span>

<span data-ttu-id="fdc11-142">Dado que las transiciones no pueden superponerse en el mismo objeto, no tienen un valor de prioridad.</span><span class="sxs-lookup"><span data-stu-id="fdc11-142">Because transitions cannot overlap on the same object, they do not have a priority value.</span></span>

<span data-ttu-id="fdc11-143">En el ejemplo siguiente se agrega el objeto de transición a una pista:</span><span class="sxs-lookup"><span data-stu-id="fdc11-143">The following example adds the transition object to a track:</span></span>


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



<span data-ttu-id="fdc11-144">En el ejemplo se consulta el objeto Track para la interfaz [**IAMTimelineTransable**](iamtimelinetransable.md) antes de llamar a AddTrans.</span><span class="sxs-lookup"><span data-stu-id="fdc11-144">The example queries the track object for the [**IAMTimelineTransable**](iamtimelinetransable.md) interface before calling AddTrans.</span></span>

<span data-ttu-id="fdc11-145">**5. establecer propiedades**</span><span class="sxs-lookup"><span data-stu-id="fdc11-145">**5. Set Properties**</span></span>

<span data-ttu-id="fdc11-146">Muchos efectos y transiciones admiten propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fdc11-146">Many effects and transitions support custom properties.</span></span> <span data-ttu-id="fdc11-147">Para obtener más información, vea [establecer propiedades en efectos y transiciones](setting-properties-on-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="fdc11-147">For information, see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md).</span></span>

<span data-ttu-id="fdc11-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdc11-148">Example</span></span>

<span data-ttu-id="fdc11-149">En el ejemplo de código siguiente se agrega una [transición de borrado de SMPTE](smpte-wipe-transition.md) a una pista. Se supone que el objeto Track ya existe en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fdc11-149">The following code example adds a [SMPTE Wipe Transition](smpte-wipe-transition.md) to a track. It assumes that the track object already exists in the timeline.</span></span>


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a><span data-ttu-id="fdc11-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fdc11-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdc11-151">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="fdc11-151">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



