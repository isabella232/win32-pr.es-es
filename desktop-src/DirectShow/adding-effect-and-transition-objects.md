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
# <a name="adding-effect-and-transition-objects"></a>Agregar objetos Effect y Transition

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En DES, un efecto o una transición se representa con dos objetos:

-   Un *objeto Timeline* representa el efecto o la transición dentro de la escala de tiempo. En el caso de los efectos, el objeto Timeline admite la interfaz [**IAMTimelineEffect**](iamtimelineeffect.md) . En el caso de las transiciones, admite la interfaz [**IAMTimelineTrans**](iamtimelinetrans.md) . Ambos tipos admiten la interfaz [**IAMTimelineObj**](iamtimelineobj.md) .
-   El *subobjeto* es un objeto que implementa el procesamiento de datos para el efecto o la transición. El objeto Timeline contiene un puntero al subobjeto.

Para agregar un efecto o una transición, realice los pasos siguientes.

**1. crear el objeto Timeline**

Para crear el objeto Timeline, llame al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Establezca el tipo igual a la **escala de tiempo del \_ \_ \_ efecto de tipo principal** para un efecto o la **\_ \_ \_ transición de tipo principal** de la escala de tiempo para una transición.

En el ejemplo siguiente se crea un objeto de transición:


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. especificar el subobjeto**

El objeto Timeline actúa como contenedor de otro objeto, denominado *subobjeto*, que realiza el trabajo real. El subobjeto implementa una transformación de datos que produce el efecto o la transición deseados. Para obtener una lista de las transiciones y los efectos proporcionados con DES, consulte [transiciones y efectos](transitions-and-effects.md).

Para establecer el subobjeto, llame al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) en el objeto Timeline, pasándole el identificador de clase (CLSID) del subobjeto. DirectShow proporciona un enumerador para los efectos de vídeo y las transiciones de vídeo, que puede usar para obtener el CLSID. Para obtener más información, consulte [enumeración de efectos y transiciones](enumerating-effects-and-transitions.md).

En el ejemplo siguiente se establece la [transición de borrado de SMPTE](smpte-wipe-transition.md) como el subobjeto:


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. establecer las horas de inicio y detención**

Para establecer las horas de inicio y detención, llame al método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) . Estas horas son relativas a la hora de inicio del objeto primario. Los efectos pueden superponerse dentro del mismo objeto, pero las transiciones no.

En el ejemplo siguiente se establece la hora de inicio en 5 segundos y la hora de detención en 10 segundos:


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Cuando se representa una transición, el progreso de la transición en cada fotograma se calcula en función de una propiedad de **progreso** , que se normaliza en un intervalo de 0,0 a 1,0. DES usa la hora de inicio de cada fotograma para calcular el valor de progreso. Esto significa que si la hora de detención de la transición es igual a la hora de detención del origen, el valor de **progreso** nunca alcanzará exactamente 1,0, porque la hora de inicio del último fotograma es ligeramente menor que la hora de detención. Para que la transición llegue a 1,0, establezca la hora de detención de la transición para que sea al menos un fotograma anterior a la hora de detención del origen.

**4. Insertar el objeto en la escala de tiempo**

Para insertar el objeto en la escala de tiempo, llame a uno de los métodos siguientes en el elemento primario, en función del tipo de objeto:

-   Efectos: [ **IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   Transiciones: [ **IAMTimelineTransable:: TransAdd**](iamtimelinetransable-transadd.md)

En el método [**IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) , debe especificar la prioridad del efecto. Cuando los efectos se superponen en el mismo objeto, se aplican en orden de prioridad. El efecto de audio de sobre de volumen es una excepción; Consulte la referencia de [efectos de sobre de volumen](volume-envelope-effect.md) para más información. Dentro de una composición, todas las pistas de audio se mezclan antes de que se apliquen los efectos de audio de la composición.

Dado que las transiciones no pueden superponerse en el mismo objeto, no tienen un valor de prioridad.

En el ejemplo siguiente se agrega el objeto de transición a una pista:


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



En el ejemplo se consulta el objeto Track para la interfaz [**IAMTimelineTransable**](iamtimelinetransable.md) antes de llamar a AddTrans.

**5. establecer propiedades**

Muchos efectos y transiciones admiten propiedades personalizadas. Para obtener más información, vea [establecer propiedades en efectos y transiciones](setting-properties-on-effects-and-transitions.md).

Ejemplo

En el ejemplo de código siguiente se agrega una [transición de borrado de SMPTE](smpte-wipe-transition.md) a una pista. Se supone que el objeto Track ya existe en la escala de tiempo.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



