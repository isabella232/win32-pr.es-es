---
description: El modelo de interfaz de proveedor de compatibilidad de seguridad (SSPI) proporciona una única interfaz para una aplicación de transporte cliente/servidor mediante los distintos paquetes de seguridad disponibles en un equipo o red.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedimientos usados con la mayoría de los paquetes y protocolos de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374995"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Procedimientos usados con la mayoría de los paquetes y protocolos de seguridad

El [*modelo de interfaz*](../secgloss/s-gly.md) de proveedor de compatibilidad de seguridad (SSPI) [](../secgloss/s-gly.md) proporciona una única interfaz para una aplicación de transporte cliente/servidor mediante los distintos paquetes de seguridad disponibles en un equipo o red. SSPI permite que una aplicación use un paquete de seguridad sin tratar con los protocolos de [*seguridad subyacentes*](../secgloss/s-gly.md) del paquete. Al mismo tiempo, SSPI también permite que aplicaciones sofisticadas que tienen en cuenta la seguridad aprovechen las funcionalidades avanzadas de paquetes de seguridad específicos.

Las aplicaciones inicializan SSPI mediante los pasos siguientes para proteger una conexión de red para la mayoría de los paquetes de seguridad:

-   [Uso de SecBufferDesc y SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Inicialización de SSPI](initializing-sspi.md)
-   [Establecimiento de una conexión segura con autenticación](establishing-a-secure-connection-with-authentication.md)
-   [Garantizar la integridad de la comunicación durante la Exchange](ensuring-communication-integrity-during-message-exchange.md)
-   [Finalización de una sesión de SSPI](ending-an-sspi-session.md)

 

 
