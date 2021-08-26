---
title: Cola de solicitudes con nombre
description: Cola de solicitudes con nombre
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2174044f23f30470f3285e3c8fcf9bd2dbd474b10c306df7f2fbb215b992eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078354"
---
# <a name="named-request-queue"></a>Cola de solicitudes con nombre

La característica de cola de solicitudes con nombre de la API del servidor HTTP versión 2.0 permite que varias aplicaciones, que funcionan en procesos y cuentas de usuario independientes, accedan a la cola de solicitudes. La cola de solicitudes se abre por nombre y se protege mediante listas de Access Control (ACL) para asegurarse de que las aplicaciones no puedan tener acceso a los datos de otros usuarios. Un único proceso crea la cola de solicitudes y concede permiso a otros procesos para usar la cola de solicitudes. Por lo tanto, otros procesos del equipo acceden a la cola de solicitudes con los privilegios mínimos necesarios para dar servicio a las solicitudes. Los posibles daños en el servicio HTTP, debido a vulnerabilidades en el código de terceros, se minimizan cuando las aplicaciones se ejecutan con privilegios mínimos.

La cola de solicitudes con nombre se crea con la [**función HttpCreateRequestQueue.**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) Cuando se crea la cola de solicitudes, la aplicación especifica la ACL en el *parámetro pSecurityAttribute.* La ACL, que solo se puede establecer cuando se crea la cola de solicitudes, permite a los procesos de trabajo abrir la cola de solicitudes, recibir solicitudes y enviar respuestas. De forma predeterminada, los procesos no pueden abrir una cola de solicitudes a menos que se les haya concedido permiso en la ACL. Las aplicaciones no requieren privilegios administrativos para crear la cola de solicitudes.

La cola de solicitudes debe crearse con un nombre especificado en el *parámetro pName* de [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) para que otros procesos abran la cola de solicitudes. Si *pName* es **NULL,** se crea una cola de solicitudes sin nombre y ningún otro proceso puede abrirlo.

## <a name="creator-and-controller-processes"></a>Procesos de creador y controlador

Cuando se crea la cola de solicitudes, la aplicación puede abrirla como un proceso de controlador o un proceso de creador. Tanto el controlador como los procesos del creador actúan como administradores de la cola de solicitudes, pero el controlador no realiza operaciones de E/S en ella. La aplicación indica que se trata de un proceso de controlador cuando se crea la cola de solicitudes **especificando HTTP \_ CREATE REQUEST QUEUE FLAG \_ \_ \_ \_ CONTROLLER** en el parámetro *Flags* [**de HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue). Si no **se establece la marca HTTP CREATE REQUEST QUEUE FLAG \_ \_ \_ \_ \_ CONTROLLER,** la aplicación es un proceso de creador.

La lista siguiente contiene las tareas realizadas por el proceso del controlador y el proceso del creador:

-   Cree la cola de solicitudes y especifique el nombre.
-   Configure la cola de solicitudes mediante la [**función HttpSetRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)
-   Consulte los parámetros de configuración de la cola de solicitudes [**mediante la función HttpQueryRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty)
-   Cree grupos de direcciones URL y asócialos a una cola de solicitudes.
-   Establezca la ACL que especifica los procesos de trabajo que pueden recibir E/S en la cola de solicitudes.
-   Llame [**a HttpWaitForDemandStart para**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) retrasar la creación de instancias de los procesos de trabajo hasta que llegue la primera solicitud a la cola de solicitudes.

Además de estas tareas, el proceso del creador también puede realizar operaciones de E/S en la cola de solicitudes.

## <a name="worker-processes"></a>Procesos de trabajo

Un proceso de trabajo puede abrir una cola de solicitudes existente solo si se les ha concedido acceso a ella en la ACL. Los procesos de trabajo que funcionan con privilegios mínimos pueden abrir una cola de solicitudes y realizar E/S en ella. Las aplicaciones abren una cola de solicitudes existente mediante una llamada a [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) con **HTTP CREATE REQUEST QUEUE FLAG OPEN \_ \_ \_ \_ \_ \_ EXISTING** en el parámetro *Flags* y el nombre de la cola de solicitudes en el *parámetro pName.*

El proceso de trabajo realiza las siguientes funciones:

-   Recibir solicitudes y enviar respuestas en la cola de solicitudes.
-   Abra una cola de solicitudes existente por nombre. El identificador de la cola de solicitudes devuelta al proceso de trabajo no se puede usar para configurar la cola de solicitudes.
-   Consulte los parámetros de configuración de la cola de solicitudes.

En el diagrama siguiente se muestra el modelo de proceso de trabajo para las colas de solicitudes. La cola de solicitudes puede tener varios procesos de trabajo que procesan E/S y uno de creador que configura la cola de solicitudes.

![modelo de proceso de trabajo para colas de solicitudes](images/namedrequestqueue.png)

 

 




