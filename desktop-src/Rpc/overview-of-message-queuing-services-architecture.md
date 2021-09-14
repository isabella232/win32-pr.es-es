---
title: Introducción a la arquitectura de Message Queuing Services
description: Message Queuing Services (MSMQ) usa un modelo de sitio o empresa. Normalmente, un sitio es una ubicación física, como un edificio. Una empresa consta de uno o varios sitios y representa una organización.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169057"
---
# <a name="overview-of-message-queuing-services-architecture"></a>Introducción a la arquitectura de Message Queuing Services

Message Queuing Services (MSMQ) usa un modelo de sitio o empresa. Normalmente, un sitio es una ubicación física, como un edificio. Una empresa consta de uno o varios sitios y representa una organización.

En el diagrama siguiente se muestra la arquitectura del servicio MSMQ.

![Arquitectura de msmq](images/msmq.png)

En el núcleo de MSMQ se encuentra la base de datos de Message Queue Information Service (MQIS), que se ejecuta sobre SQL Server. Una empresa tiene un único MQIS maestro, denominado controlador de Enterprise principal. Cada sitio tiene su propio MQIS, denominado controlador *de sitio primario* y cero o más controladores de sitio de copia de *seguridad.* Por último, están los equipos cliente individuales, cada uno de los cuales tiene su propio administrador de colas, implementado como servicio. El controlador Enterprise principal también puede ser un controlador de sitio primario y cualquier controlador también puede ser un cliente.

Las colas de mensajes pueden ser públicas o privadas. Las colas públicas se registran en Active Directory y son accesibles a través de la red. Los mensajes de una cola pública se enruta en toda la empresa, bajo el control de MSMQ. Los mensajes de la aplicación cliente se mueven desde el administrador de colas del cliente a la cola de destino al desplazarse entre los administradores de cola de los controladores de sitio.

El administrador de colas local mantiene las colas privadas y no se registran en Active Directory. El ámbito de los mensajes de cola privada se limita al equipo en el que residen.

 

 




