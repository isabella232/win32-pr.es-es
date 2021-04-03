---
title: Message Queue Server de RPC
description: Message Queuing (MSMQ) permite a los usuarios comunicarse a través de redes y sistemas independientemente del estado actual de las aplicaciones y los sistemas que se comunican.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- RPC llamada a procedimiento remoto, descripción, Message Queue Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076136"
---
# <a name="rpc-message-queuing"></a>Message Queue Server de RPC

Message Queuing (MSMQ) permite a los usuarios comunicarse a través de redes y sistemas independientemente del estado actual de las aplicaciones y los sistemas que se comunican. Las aplicaciones envían y reciben mensajes a través de las colas de mensajes que mantiene MSMQ. Las colas de mensajes continúan funcionando incluso cuando la aplicación de cliente o de servidor no se está ejecutando. Message Queue Server proporciona:

-   **Mensajería asincrónica.** Con la mensajería asincrónica de MSMQ, una aplicación cliente puede enviar un mensaje a un servidor y volver inmediatamente, incluso si el equipo de destino o el programa de servidor no responde.
-   **Entrega de mensajes garantizada.** Cuando una aplicación envía un mensaje a través de MSMQ, el mensaje llegará a su destino, aunque la aplicación de destino no se ejecute al mismo tiempo o las redes y los sistemas estén sin conexión.
-   **Enrutamiento y configuración dinámica.** MSMQ proporciona enrutamiento flexible a través de redes heterogéneas. La configuración de estas redes se puede cambiar dinámicamente sin realizar cambios importantes en los sistemas y redes.
-   **Mensajería sin conexión.** Las aplicaciones que usan MSMQ no necesitan configurar sesiones directas con las aplicaciones de destino.
-   [Seguridad](security.md). MSMQ proporciona una comunicación segura basada en la seguridad de Windows y la API de cifrado (CryptoAPI) para el cifrado y las firmas digitales.
-   **Mensajería con prioridad.** MSMQ transfiere mensajes entre redes según la prioridad, lo que permite una comunicación más rápida para aplicaciones críticas.

Microsoft RPC extiende el modelo Open Software Foundation – Data Communications Equipment (OSF-DCE) para las llamadas a procedimientos remotos, ya que permite que las aplicaciones distribuidas utilicen MSMQ como transporte y controlen muchas de sus características. Esta funcionalidad está disponible para las aplicaciones RPC convencionales y, a través de la interfaz **IRPCOptions** , a las aplicaciones com.

> [!Note]  
> Message Queue Server de RPC solo está disponible en Windows 2000. Las versiones posteriores de Windows no admiten Message Queue Server de RPC.

 

En los temas siguientes se proporciona información general sobre Message Queue Server:

-   [Información general sobre la arquitectura de servicios de Message Queue Server](overview-of-message-queuing-services-architecture.md)
-   [Propiedades de Message y Message Queue](message-and-message-queue-properties.md)
-   [Usar MSMQ como transporte RPC](using-msmq-as-an-rpc-transport.md)
-   [Requisitos del sistema para aplicaciones de Message \_ Queue Server de RPC](system-requirements-for-rpc-message-queuing-applications.md)
-   [Desarrollo de aplicaciones de RPC-Message Queue Server](developing-rpc-message-queuing-applications.md)
-   [Servicios de seguridad de MSMQ](msmq-security-services.md)

 

 




