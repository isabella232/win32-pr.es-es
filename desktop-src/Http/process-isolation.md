---
title: Aislamiento de procesos
description: La API del servidor HTTP versión 2.0 proporciona la capacidad de crear un servicio más seguro y confiable mediante el aislamiento de los procesos de trabajo que están atendiendo las solicitudes en la cola de solicitudes.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025e0829e020740aeeaf0381849b68bfde8b8244e845f9b5f24347bfa6bec1d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830085"
---
# <a name="process-isolation"></a>Aislamiento de procesos

La API del servidor HTTP versión 2.0 proporciona la capacidad de crear un servicio más seguro y confiable mediante el aislamiento de los procesos de trabajo que están atendiendo las solicitudes en la cola de solicitudes. La cola de solicitudes se crea y administra mediante un proceso de controlador o creador que controla estrictamente el acceso a ella. El proceso del controlador inicia uno o varios procesos de trabajo independientes que realizan E/S en la cola de solicitudes. El proceso del controlador se ejecuta con privilegios administrativos y configura la cola de solicitudes, mientras que el trabajo con privilegios inferiores procesa las solicitudes de acceso y servicio desde la cola de solicitudes. Esta arquitectura admite la directiva de aplicaciones que se ejecutan con "privilegios mínimos" y reduce la posibilidad de vulnerabilidades de seguridad introducidas por código de terceros que se puedan ejecutar en procesos de trabajo.

El acceso a la cola de solicitudes se concede cuando el proceso del controlador crea la cola de solicitudes con un nombre y una Access Control lista de solicitudes (ACL). Las aplicaciones web que se incluyen en la ACL pueden abrir una cola de solicitudes existente por nombre. El proceso de creador también puede ser un proceso de trabajo en la cola de solicitudes. Para obtener más información, vea el [tema Cola de solicitudes con](named-request-queue.md) nombre. En el diagrama siguiente se muestra la arquitectura de una aplicación HTTP típica que se ejecuta con el modelo de proceso de trabajo:

![Diagrama que muestra la arquitectura de una aplicación H T T P mediante el modelo de proceso de trabajo.](images/processisolation.png)

Los procesos de trabajo individuales dentro de la aplicación están aislados de otros procesos de trabajo y el proceso del controlador puede supervisar el estado de cada uno de ellos. El proceso del controlador está aislado de los procesos de trabajo. A continuación se describen los componentes de la arquitectura HTTP:

-   Proceso de creador o controlador: el proceso del controlador se puede ejecutar con o sin privilegios administrativos para supervisar el estado y configurar el servicio. Normalmente, el proceso de controlador crea una sesión de servidor único para el servicio y define los grupos de direcciones URL en la sesión del servidor. El grupo de direcciones URL al que está asociada una dirección URL determinada determina qué cola de solicitudes proporciona el espacio de nombres que indica la dirección URL determinada. El proceso del controlador también crea la cola de solicitudes e inicia los procesos de trabajo que pueden tener acceso a la cola de solicitudes.
-   Proceso de trabajo: los procesos de trabajo, iniciados por el proceso del controlador, realizan E/S en la cola de solicitudes que está asociada a las direcciones URL que a su servicio. El proceso de controlador de la ACL concede a la aplicación web acceso a la cola de solicitudes cuando se crea la cola de solicitudes. A menos que la aplicación web también sea el proceso de creador, no administra el servicio ni configura la cola de solicitudes. El proceso de controlador comunica el nombre de la cola de solicitudes al proceso de trabajo y el proceso de trabajo abre la cola de solicitudes por nombre. Los procesos de trabajo pueden cargar aplicaciones web de terceros sin introducir vulnerabilidades de seguridad en otras partes de la aplicación.
-   Cola de solicitudes: el proceso del controlador crea y configura la cola de solicitudes. El controlador especifica los procesos a los que se permite el acceso a la cola de solicitudes en la ACL cuando se crea la cola de solicitudes.
-   Sesión de servidor: el proceso de controlador normalmente crea y configura una sesión de servidor único para la aplicación. La sesión del servidor mantiene las propiedades de configuración para toda la aplicación. El proceso del controlador crea grupos de direcciones URL en la sesión del servidor.
-   Grupo de direcciones URL: el proceso del controlador crea los grupos de direcciones URL en la sesión del servidor y configura el grupo de direcciones URL independientemente de la sesión del servidor. El proceso del controlador agrega direcciones URL al grupo. Las solicitudes se enruta a la cola de solicitudes a la que está asociado el grupo de direcciones URL.

 

 




