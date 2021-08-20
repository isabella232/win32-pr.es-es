---
description: En este tema se describen las mejoras Windows 8 para colas de trabajo y subprocesos en la plataforma Microsoft Media Foundation trabajo.
ms.assetid: 9E2A1D94-BF82-488E-8297-D524683ABE17
title: Mejoras de cola de trabajo y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c8b082587c387aee6a8b07ca8f5fa8d5aea81e8f9a37f8decc0816d7a8708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062282"
---
# <a name="work-queue-and-threading-improvements"></a>Mejoras de cola de trabajo y subprocesos

En este tema se describen las mejoras Windows 8 para colas de trabajo y subprocesos en la plataforma Microsoft Media Foundation trabajo.

-   [comportamiento Windows 7](#windows-7-behavior)
    -   [Colas de trabajo](#work-queues)
    -   [Compatibilidad con MMCSS](#mmcss-support)
    -   [IMFRealTimeClient](#imfrealtimeclientex)
-   [Windows 8 Mejoras](#windows-8-improvements)
    -   [Colas de trabajo multiproceso](#multithreaded-work-queues)
    -   [Colas de trabajo de tareas compartidas](#shared-task-work-queues)
    -   [Cola de espera](#wait-queue)
    -   [Mejoras en la compatibilidad con MMCSS](#enhancements-to-mmcss-support)
    -   [IMFRealTimeClientEx](#imfrealtimeclientex)
    -   [Ramas de topología](#topology-branches)
-   [Recomendaciones](#recommendations)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="windows-7-behavior"></a>Windows comportamiento 7

En esta sección se resume el comportamiento de las Media Foundation de trabajo en Windows 7.

### <a name="work-queues"></a>Colas de trabajo

La Media Foundation de trabajo crea varias colas de trabajo estándar. Solo dos se documentan como para uso general de la aplicación:

-   **MFASYNC \_ CALLBACK \_ QUEUE \_ STANDARD**
-   **FUNCIÓN LONG DE \_ COLA DE \_ DEVOLUCIÓN DE LLAMADA \_ \_ MFASYNC**

Una aplicación o componente puede asignar nuevas colas de trabajo llamando a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) o [**MFAllocateWorkQueueEx.**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex) La **función MFAllocateWorkQueueEx** define dos tipos de cola de trabajo:

-   **MF \_ STANDARD \_ WORKQUEUE crea** una cola de trabajo sin un bucle de mensajes.
-   **MF \_ WINDOW \_ WORKQUEUE crea** una cola de trabajo con un bucle de mensajes.

Para poner en cola un elemento de trabajo, llame [**a MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). La plataforma ejecuta el elemento de trabajo invocando la implementación proporcionada por el autor de la llamada de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback). En Windows 7 y versiones anteriores, la plataforma crea un subproceso por cola de trabajo.

### <a name="mmcss-support"></a>Compatibilidad con MMCSS

El [servicio Programador](../procthread/multimedia-class-scheduler-service.md) de clases multimedia (MMCSS) administra las prioridades de subprocesos para que las aplicaciones multimedia obtengan segmentos regulares de tiempo de CPU, sin denegar los recursos de CPU a las aplicaciones de prioridad inferior. MMCSS define un conjunto de tareas *que* tienen perfiles de uso de CPU diferentes. Cuando un subproceso se une a una tarea de MMCSS, MMCSS establece la prioridad del subproceso en función de varios factores:

-   Prioridad base de la tarea, que se establece en el Registro.
-   Prioridad relativa del subproceso, que se establece en tiempo de ejecución mediante una llamada a [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).
-   Varias características en tiempo de ejecución, como si la aplicación está en primer plano y cuánto tiempo de CPU consumen los subprocesos de cada clase MMCSS.

Una aplicación puede registrar una cola de trabajo con MMCSS llamando a [**MFBeginRegisterWorkQueueWithMMCSS.**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss) Esta función toma un identificador de cola de trabajo, una clase MMCSS (nombre de tarea) y el identificador de tarea MMCSS. Internamente, llama a [**AvSetMmThreadCharacteristics con**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) el nombre de tarea y el identificador de tarea. Después de registrar una cola de trabajo con MMCSS, puede obtener el identificador de clase y tarea llamando a [**MFGetWorkQueueMMCSSClass**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcssclass) y [**MFGetWorkQueueMMCSSTaskId.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsstaskid)

La [sesión multimedia](media-session.md) proporciona acceso de nivel más alto a estas API, a través de la interfaz [**IMFWorkQueueServices.**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices) Esta interfaz proporciona dos métodos principales:

| Método                                                                                                            | Descripción                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss)   | Registra una cola de trabajo con una tarea de MMCSS. Este método es básicamente un contenedor fino alrededor de [**MFBeginRegisterWorkQueueWithMMCSS,**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss)pero puede pasar el valor **MFASYNC \_ CALLBACK \_ QUEUE \_ ALL** para registrar todas las colas de trabajo de la plataforma a la vez. |
| [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) | Registra una rama de la topología con una cola de trabajo.                                                                                                                                                                                                                                         |



 

Para registrar una rama de topología, haga lo siguiente.

1.  Establezca el [atributo MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) en el nodo de origen de la rama. Use cualquier valor definido por la aplicación.
2.  Opcionalmente, establezca **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS** para unir la cola de trabajo a una tarea de MMCSS.
3.  Llame [**a BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) en la topología resuelta.

La sesión multimedia asigna una nueva cola de trabajo para cada valor único de [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md). Para cada rama de topología, las operaciones de canalización asincrónicas se realizan en la cola de trabajo que se asigna a la rama.

### <a name="imfrealtimeclient"></a>IMFRealTimeClient

La [**interfaz IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient) está pensada para componentes de canalización que crean sus propios subprocesos o usan colas de trabajo para operaciones asincrónicas. La sesión multimedia usa esta interfaz para notificar al componente de canalización el comportamiento correcto, como se muestra a continuación:

-   Si el componente de canalización crea un subproceso de trabajo, el método [**IMFRealTimeClient::RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads) notifica al componente a qué clase MMCSS se va a unir.
-   Si el componente de canalización usa una cola de trabajo, el método [**IMFRealTimeClient::SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue) indica al componente qué cola de trabajo usar.

Normalmente, un componente de canalización usa un subproceso o una cola de trabajo para realizar tareas asincrónicas, pero no ambas.

## <a name="windows-8-improvements"></a>Windows 8 Mejoras

### <a name="multithreaded-work-queues"></a>Colas de trabajo multiproceso

En Windows 8, Media Foundation admite un nuevo tipo de cola de trabajo denominado *cola multiproceso*. Una cola multiproceso usa un grupo de subprocesos del sistema para enviar elementos de trabajo. La cola multiproceso se escala mejor que las colas de un solo subproceso anteriores. Por ejemplo,

-   Varios componentes pueden compartir una cola multiproceso sin bloquearse entre sí, lo que requiere la creación de menos subprocesos.

-   Los elementos de trabajo están optimizados para evitar cambios de contexto si ya se ha establecido un evento. Esto es más eficaz que crear sus propios subprocesos para esperar eventos.

Cuando se [**usa IMFRealTimeClientEx,**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)las aplicaciones deben evitar poner en marcha subprocesos y, en su lugar, usar las colas de trabajo. Para ello, las aplicaciones deben [**implementar SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex) y no usar [**RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) y [**UnregisterThreads.**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads)

Cuando se inicializa Media Foundation plataforma, crea una cola multiproceso con el identificador **MFASYNC \_ CALLBACK \_ QUEUE \_ MULTITHREADED**.

Una cola multiproceso no serializa los elementos de trabajo. Cada vez que un subproceso del grupo de subprocesos está disponible, se envía el siguiente elemento de trabajo de la cola. El autor de la llamada debe asegurarse de que el trabajo se serializa correctamente. Para facilitar esto, Media Foundation una cola *de trabajo serie*. Una cola serie encapsula otra cola de trabajo, pero garantiza la ejecución completamente serializada. El siguiente elemento de la cola no se envía hasta que se completa el elemento anterior.

El código siguiente crea una cola de serializador a través de la cola multiproceso de la plataforma.


```C++
DWORD workQueueID;
hr = MFAllocateSerialWorkQueue(MFASYNC_CALLBACK_QUEUE_MULTITHREADED, &workQueueID); 
```



Más de una cola serie puede encapsular la misma cola multiproceso. A continuación, las colas serie comparten el mismo grupo de subprocesos y la ejecución serializada se aplica dentro de cada cola.

Las colas de trabajo estándar que existían antes de Windows 8 ahora se implementan como colas de trabajo serie que encapsulan la cola multiproceso de la plataforma. Este cambio conserva la compatibilidad con versiones anteriores.

### <a name="shared-task-work-queues"></a>Colas de trabajo de tareas compartidas

Para trabajar correctamente con el programador del kernel, debe haber una cola de trabajo multiproceso para cada tarea de MMCSS que use. La Media Foundation asigna estos datos según sea necesario, hasta uno por tarea de MMCSS, por proceso. Para obtener la cola de trabajo compartida para una tarea de MMCSS determinada, llame a [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) y especifique el nombre de la tarea. La función busca el nombre de la tarea en una tabla. Si aún no existe una cola de trabajo para esta tarea, la función asigna una nueva cola de trabajo de MT y la une inmediatamente a la tarea MMCSS. Si ya existe una cola de trabajo para esa tarea, la función devuelve el identificador de la cola de trabajo existente.

### <a name="wait-queue"></a>Cola de espera

La *cola de espera* es una cola de trabajo de plataforma especial que espera a que se señalen los eventos. Si un componente necesita esperar a que se señale un evento, puede usar la cola de espera en lugar de crear un subproceso de trabajo para esperar en el evento.

Para usar la cola de espera, llame [**a MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem). Los parámetros incluyen el identificador de evento y [**un puntero DE TIPO IMFAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) Cuando se señala el evento, la cola de espera invoca la devolución de llamada. Hay una única cola de espera de plataforma; las aplicaciones no pueden crear sus propias colas de espera.

### <a name="enhancements-to-mmcss-support"></a>Mejoras en la compatibilidad con MMCSS

Las siguientes nuevas funciones Media Foundation de la plataforma están relacionadas con MMCSS.



| Función                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex) | Registra una cola de trabajo con MMCSS. Esta función incluye un parámetro para especificar la prioridad relativa del subproceso. Internamente, este valor se traduce en una llamada a [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).                                                                                                                                                                               |
| [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)                 | Consulta la prioridad de una cola de trabajo.                                                                                                                                                                                                                                                                                                                                                                 |
| [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)                 | Registra todas las colas de trabajo de la plataforma con una tarea de MMCSS. Esta función es similar al método [**IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS,**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) pero se puede usar sin crear una instancia de la sesión multimedia. Además, la función incluye un parámetro para especificar la prioridad del subproceso base. |



 

Las aplicaciones que usan la sesión multimedia deben establecer el atributo [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) en "Audio" para la rama de representación de audio. Establezca el atributo en "Playback" (Reproducción) para la rama de representación de vídeo.

### <a name="imfrealtimeclientex"></a>IMFRealTimeClientEx

La [**interfaz DEREDUCERealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex) reemplaza a LA PROPIEDAD DEREDUCTORealTimeClient para los componentes de canalización que realizan operaciones asincrónicas.



| Método                                                             | Descripción                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RegisterThreadsEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) | Notifica al componente que registre sus subprocesos con MMCSS. Este método es equivalente a [**IMFRealTimeClient::RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads), pero agrega un parámetro para la prioridad del subproceso base. |
| [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex)       | Notifica al componente que use una cola de trabajo específica. Este método es equivalente a [**IMFReadTimeClient::SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue), pero agrega un parámetro para la prioridad del elemento de trabajo.               |
| [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads) | Notifica al componente que anula el registro de sus subprocesos de MMCSS. Este método es idéntico al [**método IMFRealTimeClient::UnregisterThreads.**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-unregisterthreads)                                       |



 

Los componentes de canalización deben usar colas de trabajo y no crear subprocesos de trabajo por los siguientes motivos:

-   Las colas de trabajo se escalan mejor, ya que usan los grupos de subprocesos del sistema operativo.
-   La plataforma controla los detalles del registro de colas de trabajo con MMCSS.
-   Un subproceso de trabajo puede provocar fácilmente un interbloqueo que es difícil de depurar.

Además, considere la posibilidad de usar la cola de trabajo del serializador si necesita serializar las operaciones asincrónicas.

### <a name="topology-branches"></a>Ramas de topología

Si el atributo [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) registra una rama de topología con MMCSS, en Windows 8 la sesión multimedia usa las colas de trabajo mt compartidas. En versiones anteriores de Windows, la sesión multimedia asignó una nueva cola de trabajo.

Se definen dos atributos nuevos para registrar una rama de topología con MMCSS.



| Atributo                                                                            | Descripción                         |
|--------------------------------------------------------------------------------------|-------------------------------------|
| [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY](mf-toponode-workqueue-mmcss-priority.md) | Especifica la prioridad del subproceso base. |
| [MF \_ TOPONODE \_ WORKQUEUE \_ ITEM \_ PRIORITY](mf-toponode-workqueue-item-priority.md)   | Especifica la prioridad del elemento de trabajo.   |



 

## <a name="recommendations"></a>Recomendaciones

-   Las aplicaciones que usan la sesión multimedia deben establecer [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) en "Audio" para la rama de representación de audio y "Playback" para la rama de representación de vídeo.
-   Las aplicaciones que usan la sesión multimedia deben llamar [**a LANSUSOWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) en la topología.
-   Para los componentes de canalización, se recomiendan colas de trabajo en lugar de subprocesos de trabajo. Si el componente usa colas de trabajo o subprocesos de trabajo, implemente [**LAREDrealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex).
-   No cree colas de trabajo privadas, ya que esto resalte el propósito de las colas de trabajo de la plataforma. Use la cola multiproceso de plataforma o una cola serie que encapsula la cola multiproceso de la plataforma.
-   Si necesita serializar operaciones asincrónicas, use una cola serie.

## <a name="summary"></a>Resumen

Las siguientes API Media Foundation de plataforma que se relacionan con subprocesos y colas de trabajo son nuevas para Windows 8.

-   [MF \_ TOPONODE \_ WORKQUEUE \_ ITEM \_ PRIORITY](mf-toponode-workqueue-item-priority.md)
-   [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY](mf-toponode-workqueue-mmcss-priority.md)
-   [**MFAllocateSerialWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue)
-   [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex)
-   [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)
-   [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem)
-   [**MFPutWorkItem2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2)
-   [**MFPutWorkItemEx2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2)
-   [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)
-   [**MFUnregisterPlatformFromMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfunregisterplatformfrommmcss)
-   [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue)
-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Colas de trabajo](work-queues.md)
</dt> </dl>

 

 
