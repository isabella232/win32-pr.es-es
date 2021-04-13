---
title: Cola de solicitudes con nombre
description: Cola de solicitudes con nombre
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4aca045f84fe9f9e4b57365ba8831456f2dc1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357625"
---
# <a name="named-request-queue"></a>Cola de solicitudes con nombre

La característica de cola de solicitud de la API del servidor HTTP versión 2,0 permite que varias aplicaciones, que funcionan en procesos y cuentas de usuario independientes, tengan acceso a la cola de solicitudes. La cola de solicitudes se abre por nombre y se protege mediante listas de Access Control (ACL) para asegurarse de que las aplicaciones no puedan tener acceso a todos los datos de los demás. Un único proceso crea la cola de solicitudes y concede permiso a otros procesos para usar la cola de solicitudes. Por lo tanto, otros procesos del equipo tienen acceso a la cola de solicitudes con los privilegios mínimos necesarios para atender las solicitudes. Los posibles daños en el servicio HTTP, debido a vulnerabilidades en el código de terceros, se minimizan cuando las aplicaciones se ejecutan con privilegios mínimos.

La cola de solicitudes con nombre se crea con la función [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) . Cuando se crea la cola de solicitudes, la aplicación especifica la ACL en el parámetro *pSecurityAttribute* . La ACL, que solo se puede establecer cuando se crea la cola de solicitudes, permite a los procesos de trabajo abrir la cola de solicitudes, recibir solicitudes y enviar respuestas. De forma predeterminada, los procesos no pueden abrir una cola de solicitudes a menos que se les haya concedido permiso en la ACL. Las aplicaciones no requieren privilegios administrativos para crear la cola de solicitudes.

La cola de solicitudes se debe crear con un nombre especificado en el parámetro *pName* de [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) para que otros procesos puedan abrir la cola de solicitudes. Si *pName* es **null**, se crea una cola de solicitudes sin nombre y ningún otro proceso puede abrirla.

## <a name="creator-and-controller-processes"></a>Procesos de creador y controlador

Cuando se crea la cola de solicitudes, la aplicación puede abrirla como un proceso de controlador o de creador. El controlador y el creador procesan actúan como administradores de la cola de solicitudes, pero el controlador no realiza operaciones de e/s en él. La aplicación indica que se trata de un proceso de controlador cuando se crea la cola de solicitudes especificando **http \_ Create \_ request \_ Queue \_ Flag \_ Controller** en el parámetro *Flags* de [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue). Si no se establece la marca de controlador de indicador de la **\_ cola de \_ solicitudes \_ \_ \_ http Create** , la aplicación es un proceso creador.

La lista siguiente contiene las tareas realizadas por el proceso de controlador y el proceso de creador:

-   Cree la cola de solicitudes y especifique el nombre.
-   Configure la cola de solicitudes mediante la función [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .
-   Consulte los parámetros de configuración de la cola de solicitudes mediante la función [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) .
-   Crear grupos de direcciones URL y asociarlos a una cola de solicitudes.
-   Establezca la ACL especificando los procesos de trabajo que pueden recibir e/s en la cola de solicitudes.
-   Llame a [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) para retrasar la creación de instancias de procesos de trabajo hasta que la primera solicitud llegue a la cola de solicitudes.

Además de estas tareas, el proceso de creador también puede realizar operaciones de e/s en la cola de solicitudes.

## <a name="worker-processes"></a>Procesos de trabajo

Un proceso de trabajo puede abrir una cola de solicitudes existente solo si se le ha concedido acceso a ella en la ACL. Los procesos de trabajo que operan con privilegios mínimos pueden abrir una cola de solicitudes y realizar operaciones de e/s en ella. Las aplicaciones abren una cola de solicitudes existente mediante una llamada a [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) con la marca de la **cola de \_ solicitudes HTTP Create, \_ \_ \_ \_ abrir \_ existente** en el parámetro *Flags* y el nombre de la cola de solicitudes en el parámetro *pName* .

El proceso de trabajo realiza las siguientes funciones:

-   Recibir solicitudes y enviar respuestas en la cola de solicitudes.
-   Abra una cola de solicitudes existente por nombre. El identificador de la cola de solicitudes que se devuelve al proceso de trabajo no se puede usar para configurar la cola de solicitudes.
-   Consulte los parámetros de configuración de la cola de solicitudes.

En el diagrama siguiente se muestra el modelo de proceso de trabajo para las colas de solicitudes. La cola de solicitudes puede tener varios procesos de trabajo que procesan la e/s y un creador que configura la cola de solicitudes.

![modelo de proceso de trabajo para colas de solicitudes](images/namedrequestqueue.png)

 

 




