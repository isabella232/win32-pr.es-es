---
title: Inicio de la demanda en las colas de solicitudes de la versión 2,0
description: .
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d618ea3fa38a856eba743d2bf60bfbfec9a633
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995267"
---
# <a name="demand-start-on-version-20-request-queues"></a>Inicio de la demanda en las colas de solicitudes de la versión 2,0

La característica de inicio a petición de las colas de solicitudes de API de la versión 2,0 del servidor HTTP permite que la aplicación del controlador retrase la creación de instancias del proceso de trabajo hasta que la primera solicitud llegue a la cola de solicitudes. Por lo tanto, las aplicaciones pueden evitar el consumo de recursos hasta que sean necesarios. Para obtener más información acerca de la aplicación de controlador, consulte el tema [cola de solicitudes con nombre](named-request-queue.md) .

## <a name="asynchronous-demand-start"></a>Inicio de la demanda asincrónica

La aplicación de controlador llama a [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) con el identificador de la cola de solicitudes para iniciar una notificación de inicio de petición. En el caso de la finalización asincrónica, la aplicación proporciona la estructura superpuesta en el parámetro *pOverlapped* . Cuando se llama a **HttpWaitForDemandStart** de forma asincrónica, se notifica a la aplicación del controlador cuando llega la primera solicitud en la cola de solicitudes. Una vez finalizada la notificación de inicio de la demanda, la aplicación del controlador puede registrarse para otra notificación de inicio de petición en la cola de solicitudes.

La API del servidor HTTP no permite más de una notificación de inicio de demanda simultánea para una cola de solicitudes. Sin embargo, cuando se completa la notificación de inicio a petición pendiente, la aplicación llama a [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) de nuevo para iniciar varios procesos de trabajo en la cola de solicitudes. HTTP no impone limitaciones en el número de notificaciones de inicio de demanda o en el número de procesos de trabajo que operan en la cola de solicitudes. Sin embargo, las aplicaciones de controlador pueden aplicar el número de procesos de trabajo permitidos en una cola de solicitudes.

La API del servidor HTTP admite la cancelación de llamadas asincrónicas de [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) . Las aplicaciones pueden usar [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) con la estructura superpuesta suministrada en *pOverlapped* para cancelar una llamada pendiente de **HttpWaitForDemandStart** .

## <a name="synchronous-demand-start"></a>Inicio de la demanda sincrónica

No se recomienda el inicio de la demanda sincrónica porque la aplicación se bloquea hasta que llega una solicitud en la cola de solicitudes.

 

 