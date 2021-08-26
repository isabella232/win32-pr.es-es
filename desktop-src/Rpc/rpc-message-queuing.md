---
title: RPC Message Queuing
description: Message Queuing (MSMQ) permite a los usuarios comunicarse entre redes y sistemas independientemente del estado actual de las aplicaciones y los sistemas que se comunican.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- Llamada a procedimiento remoto RPC, descrita, cola de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c44296068087dc2fd4423dbb3294c3c7a417e8a983ec958c2ad765ff87ea81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018385"
---
# <a name="rpc-message-queuing"></a>RPC Message Queuing

Message Queuing (MSMQ) permite a los usuarios comunicarse entre redes y sistemas independientemente del estado actual de las aplicaciones y los sistemas que se comunican. Las aplicaciones envían y reciben mensajes a través de colas de mensajes que mantiene MSMQ. Las colas de mensajes siguen funcionando incluso cuando la aplicación cliente o servidor no se está ejecutando. Message Queuing proporciona:

-   **Mensajería asincrónica.** Con la mensajería asincrónica de MSMQ, una aplicación cliente puede enviar un mensaje a un servidor y devolverlo inmediatamente, incluso si el equipo de destino o el programa de servidor no responde.
-   **Entrega de mensajes garantizada.** Cuando una aplicación envía un mensaje a través de MSMQ, el mensaje llega a su destino incluso si la aplicación de destino no se ejecuta al mismo tiempo o las redes y sistemas están sin conexión.
-   **Enrutamiento y configuración dinámica.** MSMQ proporciona un enrutamiento flexible a través de redes heterogéneos. La configuración de estas redes se puede cambiar dinámicamente sin realizar cambios importantes en los sistemas y las propias redes.
-   **Mensajería sin conexión.** Las aplicaciones que usan MSMQ no necesitan configurar sesiones directas con aplicaciones de destino.
-   [Seguridad](security.md). MSMQ proporciona una comunicación segura basada en Windows seguridad y la API criptográfica (CryptoAPI) para el cifrado y las firmas digitales.
-   **Mensajería con prioridad.** MSMQ transfiere mensajes entre redes en función de la prioridad, lo que permite una comunicación más rápida para las aplicaciones críticas.

Microsoft RPC amplía el modelo Open Software Foundation–Data Communications Equipment (OSF-DCE) para las llamadas a procedimientos remotos al permitir que las aplicaciones distribuidas usen MSMQ como transporte y controlen muchas de sus características. Esta funcionalidad está disponible para aplicaciones RPC convencionales y, a través de la **interfaz IRPCOptions,** para aplicaciones COM.

> [!Note]  
> La cola de mensajes RPC solo está disponible Windows 2000. Las versiones posteriores Windows no admiten la cola de mensajes RPC.

 

En los temas siguientes se proporciona información general sobre la cola de mensajes:

-   [Introducción a la arquitectura de Message Queuing Services](overview-of-message-queuing-services-architecture.md)
-   [Propiedades de cola de mensajes y mensajes](message-and-message-queue-properties.md)
-   [Uso de MSMQ como transporte RPC](using-msmq-as-an-rpc-transport.md)
-   [Requisitos del sistema para aplicaciones rpc-Message \_ Queuing](system-requirements-for-rpc-message-queuing-applications.md)
-   [Desarrollo de RPC-Message queuing applications](developing-rpc-message-queuing-applications.md)
-   [Servicios de seguridad de MSMQ](msmq-security-services.md)

 

 




