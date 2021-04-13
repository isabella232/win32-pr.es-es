---
title: Cómo encaja la arquitectura de multidifusión
description: En esta sección se describe una configuración de ejemplo y cómo se ajustan los componentes principales.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269019"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Cómo encaja la arquitectura de multidifusión

En esta sección se describe una configuración de ejemplo y cómo se ajustan los componentes principales.

En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.

![relación entre los componentes del enrutador de Windows 2000](images/mrarch1.png)

El administrador del grupo de multidifusión es una parte del servicio RRAS que se ejecuta en un servidor que funciona como enrutador.

El enrutador mostrado tiene tres protocolos de enrutamiento de multidifusión (protocolo 1, protocolo 2, protocolo 3) que se ejecutan en él. Cada protocolo puede poseer una o más interfaces (en esta ilustración, el protocolo 1 es el propietario de la interfaz 1, el protocolo 2 es el propietario de la interfaz 2 y el protocolo 3 posee la interfaz 3). Cada interfaz solo puede pertenecer a un protocolo de enrutamiento (además de a IGMP, que es un caso especial).

El administrador del grupo de multidifusión se ejecuta en el enrutador y coordina la distribución de la información de grupo entre los protocolos de enrutamiento.

En la ilustración siguiente se muestra la relación entre dos enrutadores en una arquitectura de multidifusión.

![relación entre dos enrutadores en la arquitectura de multidifusión](images/mrarch2.png)

En la ilustración anterior, el enrutador 2 envía un mensaje de multidifusión a la red 2 en la interfaz 3. El enrutador 1 recibe el mensaje de multidifusión de la red 2 en la interfaz 3. En ambos enrutadores, el protocolo 3 es el propietario de la interfaz correspondiente 3.

En la ilustración siguiente se muestra la ruta de acceso a un mensaje de un origen de multidifusión (a un grupo de multidifusión) que se toma para alcanzar el host que se ha unido al grupo de multidifusión. Los enrutadores de la ilustración usan la misma configuración que las ilustraciones anteriores; sin embargo, no se muestran los detalles de la interfaz y el protocolo para que la figura sea simple.

![Ruta de acceso del mensaje del origen de multidifusión al host de destino](images/mrarch3.png)

En el siguiente escenario se describen los eventos que tienen lugar cuando un host se une a un grupo de multidifusión. Consulte la ilustración anterior para ver las relaciones entre las distintas entidades.

1.  El host 1 se une al grupo de multidifusión G en la red 3.
2.  El enrutador 3 aprende sobre G a través de IGMP.
3.  El administrador del grupo de multidifusión en el enrutador 3 notifica al protocolo 3 del enrutador 3 que hay nuevos receptores para G.
4.  Después, el protocolo 3 en el enrutador 3 notifica al protocolo 3 del enrutador 1 acerca de G.
5.  A su vez, el protocolo 3 en el enrutador 1 notifica al administrador del grupo de multidifusión en el enrutador 1 acerca de G.
6.  A continuación, el administrador del grupo de multidifusión en el enrutador 1 notifica al protocolo 1 y al protocolo 2 acerca de G.
7.  El protocolo 2 puede informar al enrutador 2 acerca de G si el protocolo está diseñado para hacerlo.

En el siguiente escenario se describen los eventos que tienen lugar cuando se envía un mensaje a un grupo de multidifusión. Consulte la ilustración anterior para ver las relaciones entre las distintas entidades.

1.  Un origen de la red 1 envía un mensaje al grupo G.
2.  El mensaje enviado desde los orígenes S va primero al enrutador 2, que, a continuación, lo reenvía al enrutador 1 mediante la interfaz 2 (ya que el protocolo 2 ha informado de que los receptores están en el nivel inferior).
3.  El enrutador 1 reenvía el mensaje al enrutador 3 (puesto que el protocolo 2 ha informado de que el enrutador 1 es el mismo que el que los receptores están presentes).
4.  El enrutador 3 reenvía el mensaje a la red 3 y, por tanto, llega al host 1.

Para obtener más información sobre la interacción del Protocolo de enrutamiento de multidifusión, consulte [RFC 2715](routing-protocols-request-for-comments.md), reglas de interoperabilidad para los protocolos de enrutamiento de multidifusión.

 

 




