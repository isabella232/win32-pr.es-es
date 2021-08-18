---
title: Cómo encaja la arquitectura de multidifusión
description: En esta sección se describe una configuración de ejemplo y cómo encajan los componentes principales.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94f4ca79b9fdd6b2e2fd9e75dc61d780af4380ed958a491f69231f7d541f0aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791326"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Cómo encaja la arquitectura de multidifusión

En esta sección se describe una configuración de ejemplo y cómo encajan los componentes principales.

En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.

![relación entre los componentes del enrutador de Windows 2000](images/mrarch1.png)

El administrador de grupos de multidifusión forma parte del servicio RRAS que se ejecuta en un servidor que funciona como enrutador.

El enrutador que se muestra tiene tres protocolos de enrutamiento de multidifusión (Protocolo 1, Protocolo 2, Protocolo 3) ejecutándose en él. Cada protocolo puede ser propietario de una o varias interfaces (en esta ilustración, el protocolo 1 posee la interfaz 1, el protocolo 2 posee la interfaz 2 y el protocolo 3 es el propietario de la interfaz 3). Cada interfaz solo puede pertenecer a un protocolo de enrutamiento (además de IGMP, que es un caso especial).

El administrador de grupos de multidifusión se ejecuta en el enrutador y coordina la distribución de información de grupo entre los protocolos de enrutamiento.

En la ilustración siguiente se muestra la relación entre dos enrutadores en una arquitectura de multidifusión.

![relación entre dos enrutadores en la arquitectura de multidifusión](images/mrarch2.png)

En la ilustración anterior, el enrutador 2 envía un mensaje de multidifusión a la red 2 en la interfaz 3. El enrutador 1 recibe el mensaje de multidifusión de la red 2 en la interfaz 3. En ambos enrutadores, el Protocolo 3 posee la interfaz 3 correspondiente.

En la ilustración siguiente se muestra la ruta de acceso que un mensaje de un origen de multidifusión (a un grupo de multidifusión) toma para llegar al host que se ha unido al grupo de multidifusión. Los enrutadores de la ilustración usan la misma configuración que las ilustraciones anteriores. sin embargo, los detalles de la interfaz y el protocolo no se muestran para que la figura sea sencilla.

![ruta de acceso del mensaje del origen de multidifusión al host de destino](images/mrarch3.png)

En el escenario siguiente se describen los eventos que tienen lugar cuando un host se une a un grupo de multidifusión. Consulte la ilustración anterior para ver las relaciones entre las distintas entidades.

1.  El host 1 se une al grupo de multidifusión G en la red 3.
2.  El enrutador 3 aprende sobre G a través de IGMP.
3.  El administrador de grupos de multidifusión del enrutador 3 notifica al Protocolo 3 en el enrutador 3 que hay nuevos receptores para G.
4.  A continuación, el protocolo 3 del enrutador 3 notifica al protocolo 3 en el enrutador 1 sobre G.
5.  A su vez, el protocolo 3 en el enrutador 1 notifica al administrador de grupos de multidifusión en el enrutador 1 sobre G.
6.  A continuación, el administrador de grupos de multidifusión del enrutador 1 notifica a Protocolo 1 y Protocolo 2 sobre G.
7.  El protocolo 2 puede informar al enrutador 2 sobre G, si el protocolo está diseñado para ello.

En el siguiente escenario se describen los eventos que tienen lugar cuando se envía un mensaje a un grupo de multidifusión. Consulte la ilustración anterior para ver las relaciones entre las distintas entidades.

1.  Un origen de la red 1 envía un mensaje al grupo G.
2.  El mensaje enviado desde el origen S va primero al enrutador 2, que luego lo reenvía al enrutador 1 mediante la interfaz 2 (dado que el protocolo 2 ha informado al enrutador 2 de que los receptores están presentes en la bajada).
3.  El enrutador 1 reenvía el mensaje al enrutador 3 (puesto que el protocolo 2 ha informado al enrutador 1 de que los receptores están presentes en la bajada).
4.  El enrutador 3 reenvía el mensaje a la red 3 y, por tanto, llega al host 1.

Para obtener más información sobre la interacción del protocolo de enrutamiento de multidifusión, [vea RFC 2715](routing-protocols-request-for-comments.md), Reglas de interoperabilidad para protocolos de enrutamiento de multidifusión.

 

 




