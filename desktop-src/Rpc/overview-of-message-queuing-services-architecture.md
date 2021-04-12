---
title: Información general sobre la arquitectura de servicios de Message Queue Server
description: Los servicios de Message Queue Server (MSMQ) utilizan un modelo de sitio/empresa. Normalmente, un sitio es una ubicación física, como un edificio. Una empresa se compone de uno o varios sitios y representa una organización.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357445"
---
# <a name="overview-of-message-queuing-services-architecture"></a>Información general sobre la arquitectura de servicios de Message Queue Server

Los servicios de Message Queue Server (MSMQ) utilizan un modelo de sitio/empresa. Normalmente, un sitio es una ubicación física, como un edificio. Una empresa se compone de uno o varios sitios y representa una organización.

En el diagrama siguiente se ilustra la arquitectura del servicio MSMQ.

![arquitectura de MSMQ](images/msmq.png)

En esencia, MSMQ es la base de datos del servicio de información de cola de mensajes (MQIS), que se ejecuta sobre SQL Server. Una empresa tiene un solo MQIS maestro, denominado controlador Enterprise principal. Cada sitio tiene su propio MQIS, denominado *controlador de sitio principal* y cero o más *controladores de sitio de copia de seguridad*. Por último, hay equipos cliente individuales, cada uno de los cuales tiene su propio administrador de cola, que se implementa como un servicio. El controlador de empresa principal también puede ser un controlador de sitio principal y cualquier controlador también puede ser un cliente.

Las colas de mensajes pueden ser públicas o privadas. Las colas públicas se registran en Active Directory y son accesibles a través de la red. Los mensajes de una cola pública se enrutan por toda la empresa, bajo el control de MSMQ. Los mensajes de aplicación cliente se mueven desde el administrador de cola del cliente a la cola de destino al viajar entre los administradores de cola de los controladores de sitio.

El administrador de cola local mantiene las colas privadas y no se registran en Active Directory. El ámbito de los mensajes de cola privados se limita al equipo en el que residen.

 

 




