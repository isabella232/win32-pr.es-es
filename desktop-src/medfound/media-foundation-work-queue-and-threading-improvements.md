---
description: En este tema se describen las mejoras de Windows 8 para las colas de trabajo y los subprocesos en la plataforma Microsoft Media Foundation.
ms.assetid: 9E2A1D94-BF82-488E-8297-D524683ABE17
title: Mejoras en la cola de trabajo y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b307cb00316696e075e9e9cc2a138e98e149be
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104083584"
---
# <a name="work-queue-and-threading-improvements"></a>Mejoras en la cola de trabajo y subprocesos

En este tema se describen las mejoras de Windows 8 para las colas de trabajo y los subprocesos en la plataforma Microsoft Media Foundation.

-   [Comportamiento de Windows 7](#windows-7-behavior)
    -   [Colas de trabajo](#work-queues)
    -   [Compatibilidad con MMCSS](#mmcss-support)
    -   [IMFRealTimeClient](#imfrealtimeclientex)
-   [Mejoras en Windows 8](#windows-8-improvements)
    -   [Colas de trabajos multiproceso](#multithreaded-work-queues)
    -   [Colas de trabajo de tareas compartidas](#shared-task-work-queues)
    -   [Cola de espera](#wait-queue)
    -   [Mejoras en la compatibilidad con MMCSS](#enhancements-to-mmcss-support)
    -   [IMFRealTimeClientEx](#imfrealtimeclientex)
    -   [Ramas de topología](#topology-branches)
-   [Recomendaciones](#recommendations)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="windows-7-behavior"></a>Comportamiento de Windows 7

En esta sección se resume el comportamiento de Media Foundation colas de trabajo en Windows 7.

### <a name="work-queues"></a>Colas de trabajo

La plataforma Media Foundation crea varias colas de trabajo estándar. Solo dos están documentados para el uso general de la aplicación:

-   **estándar de cola de devolución de \_ llamada MFASYNC \_ \_**
-   **MFASYNC \_ \_ función Long de cola de devolución de llamada \_ \_**

Una aplicación o componente puede asignar nuevas colas de trabajo mediante una llamada a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) o [**MFAllocateWorkQueueEx**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex). La función **MFAllocateWorkQueueEx** define dos tipos de cola de trabajo:

-   **MF \_ STANDARD \_ WORKQUEUE** crea una cola de trabajo sin un bucle de mensajes.
-   **MF \_ WINDOW \_ WORKQUEUE** crea una cola de trabajo con un bucle de mensajes.

Para poner en cola un elemento de trabajo, llame a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). La plataforma ejecuta el elemento de trabajo invocando la implementación proporcionada por el llamador de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback). En Windows 7 y versiones anteriores, la plataforma crea un subproceso por cada cola de trabajo.

### <a name="mmcss-support"></a>Compatibilidad con MMCSS

El [servicio Programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) administra las prioridades de los subprocesos para que las aplicaciones multimedia obtengan intervalos regulares de tiempo de CPU, sin denegar recursos de CPU a aplicaciones de menor prioridad. MMCSS define un conjunto de *tareas* que tienen distintos perfiles de uso de CPU. Cuando un subproceso se une a una tarea MMCSS, MMCSS establece la prioridad del subproceso en función de varios factores:

-   La prioridad base de la tarea, que se establece en el registro.
-   La prioridad relativa del subproceso, que se establece en tiempo de ejecución mediante una llamada a [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).
-   Varias características en tiempo de ejecución, como si la aplicación está en primer plano, y cuánto tiempo de CPU se consumen los subprocesos en cada clase MMCSS.

Una aplicación puede registrar una cola de trabajo con MMCSS llamando a [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss). Esta función toma un identificador de cola de trabajo, una clase MMCSS (nombre de tarea) y el identificador de la tarea MMCSS. Internamente, llama a [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) con el nombre de tarea y el identificador de tarea. Después de registrar una cola de trabajo con MMCSS, puede obtener el identificador de la clase y de la tarea mediante una llamada a [**MFGetWorkQueueMMCSSClass**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcssclass) y [**MFGetWorkQueueMMCSSTaskId**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsstaskid).

La [sesión multimedia](media-session.md) proporciona acceso de nivel más alto a estas API a través de la interfaz [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices) . Esta interfaz proporciona dos métodos principales:

| Método                                                                                                            | Descripción                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss)   | Registra una cola de trabajo con una tarea MMCSS. Este método es esencialmente un contenedor fino en torno a [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss), pero puede pasar el valor **MFASYNC cola de devolución de \_ llamada \_ \_ All** para registrar todas las colas de trabajo de la plataforma a la vez. |
| [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) | Registra una rama de la topología con una cola de trabajo.                                                                                                                                                                                                                                         |



 

Para registrar una rama de topología, haga lo siguiente.

1.  Establezca el atributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) en el nodo de origen de la rama. Use cualquier valor definido por la aplicación.
2.  Opcionalmente, establezca la **\_ clase MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS** para unir la cola de trabajo a una tarea MMCSS.
3.  Llame a [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) en la topología resuelta.

La sesión multimedia asigna una nueva cola de trabajo para cada valor único de [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md). Para cada bifurcación de topología, las operaciones asincrónicas de canalización se realizan en la cola de trabajo asignada a la rama.

### <a name="imfrealtimeclient"></a>IMFRealTimeClient

La interfaz [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient) está pensada para los componentes de canalización que crean sus propios subprocesos o utilizan colas de trabajo para operaciones asincrónicas. La sesión multimedia utiliza esta interfaz para notificar al componente de canalización el comportamiento correcto, como se indica a continuación:

-   Si el componente de canalización crea un subproceso de trabajo, el método [**IMFRealTimeClient:: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads) notifica al componente en el que se va a unir la clase MMCSS.
-   Si el componente de canalización usa una cola de trabajo, el método [**IMFRealTimeClient:: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue) indica al componente la cola de trabajo que se va a utilizar.

Normalmente, un componente de canalización utiliza un subproceso o una cola de trabajo para realizar tareas asincrónicas, pero no ambos.

## <a name="windows-8-improvements"></a>Mejoras en Windows 8

### <a name="multithreaded-work-queues"></a>Colas de trabajos multiproceso

En Windows 8, Media Foundation admite un nuevo tipo de cola de trabajo denominada *cola multiproceso*. Una cola multiproceso utiliza un grupo de subprocesos del sistema para distribuir los elementos de trabajo. La cola multiproceso escala mejor que las anteriores colas de un solo subproceso. Por ejemplo,

-   Varios componentes pueden compartir una cola multiproceso sin bloquearse entre sí, lo que requiere la creación de menos subprocesos.

-   Los elementos de trabajo están optimizados para evitar los cambios de contexto si ya se ha establecido un evento. Esto es más eficaz que crear sus propios subprocesos para esperar en los eventos.

Al usar [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex), las aplicaciones deben evitar la rotación de subprocesos y, en su lugar, deben usar las colas de trabajo. Para ello, las aplicaciones deben implementar [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex) y no usar [**RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) y [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads).

Cuando se inicializa la plataforma de Media Foundation, se crea una cola multiproceso con el identificador MFASYNC de **la \_ cola de devolución de llamada \_ \_ multiproceso**.

Una cola multiproceso no serializa los elementos de trabajo. Cada vez que un subproceso del grupo de subprocesos está disponible, se envía el siguiente elemento de trabajo de la cola. El llamador debe asegurarse de que el trabajo se serialice correctamente. Para facilitar esta tarea, Media Foundation define una *cola de trabajo en serie*. Una cola de serie ajusta otra cola de trabajo, pero garantiza una ejecución totalmente serializada. El siguiente elemento de la cola no se envía hasta que se completa el elemento anterior.

En el código siguiente se crea una cola de serializador a través de la cola multiproceso de plataforma.


```C++
DWORD workQueueID;
hr = MFAllocateSerialWorkQueue(MFASYNC_CALLBACK_QUEUE_MULTITHREADED, &workQueueID); 
```



Varias colas de serie pueden contener la misma cola multiproceso. A continuación, las colas en serie comparten el mismo grupo de subprocesos y la ejecución serializada se aplica dentro de cada cola.

Las colas de trabajo estándar que existían antes de Windows 8 se implementan ahora como colas de trabajo en serie que encapsulan la cola multiproceso de la plataforma. Este cambio conserva la compatibilidad con versiones anteriores.

### <a name="shared-task-work-queues"></a>Colas de trabajo de tareas compartidas

Para que funcione correctamente con el programador del kernel, debe haber una cola de trabajo multiproceso para cada tarea de MMCSS que use. La plataforma Media Foundation las asigna según sea necesario, hasta una por cada tarea de MMCSS, por proceso. Para obtener la cola de trabajo compartida para una tarea de MMCSS determinada, llame a [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) y especifique el nombre de la tarea. La función busca el nombre de la tarea en una tabla. Si aún no existe una cola de trabajo para esta tarea, la función asigna una nueva cola de trabajo de MT y la une inmediatamente a la tarea MMCSS. Si ya existe una cola de trabajo para esa tarea, la función devuelve el identificador de la cola de trabajo existente.

### <a name="wait-queue"></a>Cola de espera

La *cola de espera* es una cola de trabajo de plataforma especial que espera a que se señalen los eventos. Si un componente necesita esperar a que se señalice un evento, puede utilizar la cola de espera en lugar de crear un subproceso de trabajo para esperar en el evento.

Para usar la cola de espera, llame a [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem). Los parámetros incluyen el identificador de eventos y un puntero [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Cuando se señala el evento, la cola de espera invoca la devolución de llamada. Hay una única cola de espera de plataforma; las aplicaciones no pueden crear sus propias colas de espera.

### <a name="enhancements-to-mmcss-support"></a>Mejoras en la compatibilidad con MMCSS

Las siguientes funciones nuevas de la plataforma Media Foundation se relacionan con MMCSS.



| Función                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex) | Registra una cola de trabajo con MMCSS. Esta función incluye un parámetro para especificar la prioridad relativa del subproceso. Internamente, este valor se convierte en una llamada a [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).                                                                                                                                                                               |
| [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)                 | Consulta la prioridad de una cola de trabajo.                                                                                                                                                                                                                                                                                                                                                                 |
| [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)                 | Registra todas las colas de trabajo de la plataforma con una tarea MMCSS. Esta función es similar al método [**IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) , pero se puede usar sin crear una instancia de la sesión multimedia. Además, la función incluye un parámetro para especificar la prioridad base del subproceso. |



 

Las aplicaciones que usan la sesión multimedia deben establecer el atributo de [ \_ clase MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) en "audio" para la rama de representación de audio. Establezca el atributo en "reproducción" para la rama de representación de vídeo.

### <a name="imfrealtimeclientex"></a>IMFRealTimeClientEx

La interfaz [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex) para reemplazar IMFRealTimeClient, para los componentes de canalización que realizan operaciones asincrónicas.



| Método                                                             | Descripción                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RegisterThreadsEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) | Notifica al componente que registre sus subprocesos con MMCSS. Este método es equivalente a [**IMFRealTimeClient:: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads), pero agrega un parámetro para la prioridad base del subproceso. |
| [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex)       | Notifica al componente que use una cola de trabajo específica. Este método es equivalente a [**IMFReadTimeClient:: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue), pero agrega un parámetro para la prioridad del elemento de trabajo.               |
| [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads) | Notifica al componente que debe anular el registro de sus subprocesos de MMCSS. Este método es idéntico al método [**IMFRealTimeClient:: UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-unregisterthreads) .                                       |



 

Los componentes de canalización deben usar colas de trabajo y no deben crear subprocesos de trabajo, por las razones siguientes:

-   Las colas de trabajos se escalan mejor, porque usan los grupos de subprocesos del sistema operativo.
-   La plataforma controla los detalles del registro de colas de trabajo con MMCSS.
-   Un subproceso de trabajo puede producir fácilmente un interbloqueo que es difícil de depurar.

Además, considere la posibilidad de usar la cola de trabajo del serializador si necesita serializar las operaciones asincrónicas.

### <a name="topology-branches"></a>Ramas de topología

Si el atributo de [ \_ clase MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) registra una rama de topología con MMCSS, en Windows 8 la sesión multimedia utiliza las colas de trabajo de MT compartidas. En versiones anteriores de Windows, la sesión multimedia asignaba una nueva cola de trabajo.

Se definen dos nuevos atributos para registrar una rama de topología con MMCSS.



| Atributo                                                                            | Descripción                         |
|--------------------------------------------------------------------------------------|-------------------------------------|
| [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ prioridad](mf-toponode-workqueue-mmcss-priority.md) | Especifica la prioridad de subproceso base. |
| [\_TOPONODE MF \_ WORKQUEUE \_ prioridad del elemento \_](mf-toponode-workqueue-item-priority.md)   | Especifica la prioridad del elemento de trabajo.   |



 

## <a name="recommendations"></a>Recomendaciones

-   Las aplicaciones que usan la sesión multimedia deben establecer la [ \_ clase MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) en "audio" para la rama de representación de audio y la "reproducción" de la rama de representación de vídeo.
-   Las aplicaciones que usan la sesión multimedia deben llamar a [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) en la topología.
-   En el caso de los componentes de canalización, se recomienda usar colas de trabajo en lugar de subprocesos de trabajo. Si el componente usa colas de trabajo o subprocesos de trabajo, implemente [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex).
-   No cree colas de trabajo privadas, ya que esto impide el propósito de las colas de trabajo de la plataforma. Use la cola multiproceso de la plataforma o una cola en serie que incluya la cola multiproceso de la plataforma.
-   Si necesita serializar operaciones asincrónicas, utilice una cola en serie.

## <a name="summary"></a>Resumen

Las siguientes API de la plataforma Media Foundation que se relacionan con los subprocesos y las colas de trabajos son nuevas en Windows 8.

-   [\_TOPONODE MF \_ WORKQUEUE \_ prioridad del elemento \_](mf-toponode-workqueue-item-priority.md)
-   [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ prioridad](mf-toponode-workqueue-mmcss-priority.md)
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

 

 
