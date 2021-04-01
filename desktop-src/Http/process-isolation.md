---
title: Aislamiento de procesos
description: La API del servidor HTTP versión 2,0 proporciona la capacidad de crear un servicio más seguro y más confiable aislando los procesos de trabajo que atienden las solicitudes en la cola de solicitudes.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efcfccc78bbef435aa0c74e918003383135bc4ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "103913962"
---
# <a name="process-isolation"></a>Aislamiento de procesos

La API del servidor HTTP versión 2,0 proporciona la capacidad de crear un servicio más seguro y más confiable aislando los procesos de trabajo que atienden las solicitudes en la cola de solicitudes. La cola de solicitudes se crea y administra mediante un proceso de controlador o creador que controla estrictamente el acceso a ella. El proceso del controlador inicia uno o varios procesos de trabajo independientes que realizan la e/s en la cola de solicitudes. El proceso del controlador se ejecuta con privilegios administrativos y configura la cola de solicitudes, mientras que el trabajador con menos privilegios procesa el acceso y las solicitudes de servicio de la cola de solicitudes. Esta arquitectura es compatible con la Directiva de aplicaciones que se ejecutan en "privilegios mínimos" y reduce la posibilidad de que se produzcan vulnerabilidades de seguridad presentadas por código de terceros que se puede estar ejecutando en procesos de trabajo.

Se concede acceso a la cola de solicitudes cuando el proceso de controlador crea la cola de solicitudes con un nombre y una lista de Access Control (ACL). Las aplicaciones web que se incluyen en la ACL pueden abrir una cola de solicitudes existente por nombre. El proceso creador también puede ser un proceso de trabajo en la cola de solicitudes. Para obtener más información, vea el tema [cola de solicitudes con nombre](named-request-queue.md) . En el diagrama siguiente se muestra la arquitectura de una aplicación HTTP típica que se ejecuta con el modelo de proceso de trabajo:

![Diagrama que muestra la arquitectura de una aplicación H T t P mediante el modelo de proceso de trabajo.](images/processisolation.png)

Los procesos de trabajo individuales dentro de la aplicación están aislados de otros procesos de trabajo y el proceso del controlador puede supervisar el estado de cada uno de los procesos de trabajo. El proceso del controlador está aislado de los procesos de trabajo. A continuación se describen los componentes de la arquitectura HTTP:

-   Proceso del creador o controlador: el proceso del controlador puede ejecutarse con privilegios administrativos, o sin ellos, para supervisar el estado y configurar el servicio. Normalmente, el proceso de controlador crea una única sesión de servidor para el servicio y define los grupos de direcciones URL en la sesión de servidor. El grupo de direcciones URL al que está asociada una dirección URL determinada determina qué servicio de cola de solicitudes es el espacio de nombres denotado por la dirección URL determinada. El proceso del controlador también crea la cola de solicitudes e inicia los procesos de trabajo que pueden tener acceso a la cola de solicitudes.
-   Proceso de trabajo: los procesos de trabajo, iniciados por el proceso del controlador, realizan la e/s en la cola de solicitudes que está asociada a las direcciones URL que prestan servicio. El proceso del controlador de la ACL concede a la aplicación web acceso a la cola de solicitudes cuando se crea la cola de solicitudes. A menos que la aplicación web sea también el proceso de creador, no administra el servicio ni configura la cola de solicitudes. El proceso del controlador comunica el nombre de la cola de solicitudes al proceso de trabajo y el proceso de trabajo abre la cola de solicitudes por nombre. Los procesos de trabajo pueden cargar aplicaciones Web de terceros sin introducir vulnerabilidades de seguridad en otras partes de la aplicación.
-   Cola de solicitudes: el proceso del controlador crea y configura la cola de solicitudes. El controlador especifica los procesos a los que se permite el acceso a la cola de solicitudes en la ACL cuando se crea la cola de solicitudes.
-   Sesión de servidor: el proceso del controlador normalmente crea y configura una sesión de un solo servidor para la aplicación. La sesión del servidor mantiene las propiedades de configuración de toda la aplicación. El proceso del controlador crea los grupos de direcciones URL en la sesión del servidor.
-   Grupo de direcciones URL: el proceso de controlador crea los grupos de direcciones URL en la sesión de servidor y configura el grupo de direcciones URL de manera independiente de la sesión de servidor. El proceso del controlador agrega las direcciones URL al grupo. Las solicitudes se enrutan a la cola de solicitudes a la que está asociado el grupo de direcciones URL.

 

 




