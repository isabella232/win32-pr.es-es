---
description: El modelo de interfaz del proveedor de compatibilidad para seguridad (SSPI) proporciona una única interfaz para una aplicación de transporte de cliente/servidor mediante los diversos paquetes de seguridad disponibles en un equipo o una red.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedimientos utilizados con la mayoría de los protocolos y paquetes de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541163"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Procedimientos utilizados con la mayoría de los protocolos y paquetes de seguridad

El modelo de [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) proporciona una única interfaz para una aplicación de transporte de cliente/servidor mediante los diversos paquetes de [*seguridad*](../secgloss/s-gly.md) disponibles en un equipo o una red. SSPI permite a una aplicación usar un paquete de seguridad sin tratar con los [*protocolos de seguridad*](../secgloss/s-gly.md) subyacentes del paquete. Al mismo tiempo, SSPI también permite que las aplicaciones sofisticadas con reconocimiento de la seguridad aprovechen las capacidades avanzadas de los paquetes de seguridad específicos.

Las aplicaciones inicializan SSPI mediante los pasos siguientes para proteger una conexión de red para la mayoría de los paquetes de seguridad:

-   [Usar SecBufferDesc y SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Inicializando SSPI](initializing-sspi.md)
-   [Establecer una conexión segura con la autenticación](establishing-a-secure-connection-with-authentication.md)
-   [Garantizar la integridad de la comunicación durante el intercambio de mensajes](ensuring-communication-integrity-during-message-exchange.md)
-   [Finalizar una sesión SSPI](ending-an-sspi-session.md)

 

 
