---
description: Agregar objetos de efecto y transición
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Agregar objetos de efecto y transición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162398"
---
# <a name="adding-effect-and-transition-objects"></a>Agregar objetos de efecto y transición

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En DES, un efecto o transición se representa con dos objetos:

-   Un *objeto de escala de* tiempo representa el efecto o la transición dentro de la escala de tiempo. Para los efectos, el objeto timeline admite la [**interfaz IAMTimelineEffect.**](iamtimelineeffect.md) Para las transiciones, admite la [**interfaz IAMTimelineTrans.**](iamtimelinetrans.md) Ambos tipos admiten la [**interfaz IAMTimelineObj.**](iamtimelineobj.md)
-   El *subobjeto* es un objeto que implementa el procesamiento de datos para el efecto o la transición. El objeto de escala de tiempo contiene un puntero al subobjeto.

Para agregar un efecto o una transición, realice los pasos siguientes.

**1. Crear el objeto timeline**

Para crear el objeto timeline, llame al [**método IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md) Establezca el tipo igual a **TIMELINE MAJOR \_ TYPE \_ \_ EFFECT** para un efecto o **TIMELINE MAJOR TYPE \_ \_ \_ TRANSITION** para una transición.

En el ejemplo siguiente se crea un objeto de transición:


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. Especificar el subobjeto**

El objeto de escala de tiempo actúa como un contenedor para otro objeto, denominado *subobjeto*, que realiza el trabajo real. El subobjeto implementa una transformación de datos que genera el efecto o la transición deseados. Para obtener una lista de transiciones y efectos proporcionados con DES, vea [Transiciones y efectos.](transitions-and-effects.md)

Para establecer el subobjeto, llame al método [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) en el objeto de escala de tiempo, pasando el identificador de clase (CLSID) del subobjeto. DirectShow proporciona un enumerador para efectos de vídeo y transiciones de vídeo, que puede usar para obtener el CLSID. Para obtener más información, [vea Enumerar efectos y transiciones.](enumerating-effects-and-transitions.md)

En el ejemplo siguiente se establece la transición de borrado de [SMPTE](smpte-wipe-transition.md) como subobjeto :


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. Establecer las horas de inicio y de detenerse**

Para establecer las horas de inicio y de detenerse, llame al [**método IAMTimelineObj::SetStartStop.**](iamtimelineobj-setstartstop.md) Estas horas son relativas a la hora de inicio del objeto primario. Los efectos pueden superponerse dentro del mismo objeto, pero las transiciones no.

En el ejemplo siguiente se establece la hora de inicio en 5 segundos y la hora de detenerse en 10 segundos:


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Cuando se representa una transición, el progreso de la transición en cada fotograma se calcula en función de una propiedad **Progress,** que se normaliza a un intervalo de 0,0 a 1,0. DES usa la hora de inicio de cada fotograma para calcular el valor de progreso. Esto significa que si la hora de detenerse de la transición es igual a la hora de detenerse de origen, el valor de **Progreso** nunca alcanzará exactamente 1,0, porque la hora de inicio del último fotograma es ligeramente superior a la hora de detenerse. Para que la transición alcance la versión 1.0, establezca la hora de detenerse de la transición en al menos un fotograma antes de la hora de detenerse de origen.

**4. Insertar el objeto en la escala de tiempo**

Para insertar el objeto en la escala de tiempo, llame a uno de los métodos siguientes en el elemento primario, según el tipo de objeto:

-   Efectos: [ **IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   Transiciones: [ **IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)

En el [**método IAMTimelineEffectable::EffectInsBefore,**](iamtimelineeffectable-effectinsbefore.md) debe especificar la prioridad del efecto. Cuando los efectos se superponen en el mismo objeto, se aplican en orden de prioridad. El efecto de audio Sobre de volumen es una excepción; Consulte la referencia [del efecto de sobre de](volume-envelope-effect.md) volumen para obtener más información. Dentro de una composición, todas las pistas de audio se mezclan antes de que se apliquen los efectos de audio para esa composición.

Dado que las transiciones no se pueden superponer en el mismo objeto, no tienen un valor de prioridad.

En el ejemplo siguiente se agrega el objeto de transición a una pista:


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



En el ejemplo se consulta el objeto track para la [**interfaz IAMTimelineTransable**](iamtimelinetransable.md) antes de llamar a AddTrans.

**5. Establecer propiedades**

Muchos efectos y transiciones admiten propiedades personalizadas. Para obtener información, vea [Establecer propiedades en efectos y transiciones.](setting-properties-on-effects-and-transitions.md)

Ejemplo

En el ejemplo de código siguiente se agrega una transición de [borrado de SMPTE](smpte-wipe-transition.md) a una pista. Se supone que el objeto de seguimiento ya existe en la escala de tiempo.


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

 

 



