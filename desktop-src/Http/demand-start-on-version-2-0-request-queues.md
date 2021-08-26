---
title: Inicio de la demanda en las colas de solicitudes de la versión 2.0
description: Inicio de la demanda en las colas de solicitudes de la versión 2.0
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ec5f0d2d973cfb7d4d0a3f23a5d1f6b6c6055dd9aff19521ed9ff100879c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050795"
---
# <a name="demand-start-on-version-20-request-queues"></a>Inicio de la demanda en las colas de solicitudes de la versión 2.0

La característica de inicio de la demanda de las colas de solicitudes de API del servidor HTTP versión 2.0 permite que la aplicación del controlador retrase la creación de instancias del proceso de trabajo hasta que la primera solicitud llegue a la cola de solicitudes. Por lo tanto, las aplicaciones pueden evitar el consumo de recursos hasta que se requieran. Para obtener más información sobre la aplicación de controlador, vea el [tema Cola de solicitudes con](named-request-queue.md) nombre.

## <a name="asynchronous-demand-start"></a>Inicio de la demanda asincrónica

La aplicación del controlador llama a [**HttpWaitForDemandStart con**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) el identificador de la cola de solicitudes para iniciar una notificación de inicio de la demanda. Para la finalización asincrónica, la aplicación proporciona la estructura superpuesta en el *parámetro pOverlapped.* Cuando **se llama a HttpWaitForDemandStart** de forma asincrónica, se notifica a la aplicación del controlador cuando la primera solicitud llega a la cola de solicitudes. Una vez completada la notificación de inicio de la demanda, la aplicación del controlador puede registrarse para otra notificación de inicio de la demanda en la cola de solicitudes.

La API del servidor HTTP no permite más de una notificación de inicio de demanda simultánea para una cola de solicitudes. Sin embargo, cuando se completa la notificación de inicio de demanda pendiente, la aplicación llama de nuevo a [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) para iniciar varios procesos de trabajo en la cola de solicitudes. HTTP no impone limitaciones en el número de notificaciones de inicio de la demanda ni en el número de procesos de trabajo que funcionan en la cola de solicitudes. Sin embargo, las aplicaciones de controlador pueden aplicar el número de procesos de trabajo permitidos en una cola de solicitudes.

La API del servidor HTTP admite la cancelación de llamadas [**httpWaitForDemandStart asincrónicas.**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) Las aplicaciones pueden [**usar CancelIoEx con**](/windows/desktop/FileIO/cancelioex-func) la estructura superpuesta proporcionada en *pOverlapped* para cancelar una llamada **a HttpWaitForDemandStart** pendiente.

## <a name="synchronous-demand-start"></a>Inicio de demanda sincrónica

No se recomienda iniciar la demanda sincrónica porque la aplicación se bloquea hasta que llega una solicitud a la cola de solicitudes.

 

 
