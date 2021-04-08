---
description: Un programa de servicio contiene código ejecutable para uno o más servicios.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912805"
---
# <a name="service-programs"></a>Programas de servicio

Un *programa de servicio* contiene código ejecutable para uno o más servicios. Un programa de servicio creado con el \_ \_ propio \_ proceso de Win32 de servicio de tipo contiene el código de un solo servicio. Un programa de servicio creado con el \_ proceso de \_ recurso compartido \_ de Win32 de servicio de tipo contiene código para más de un servicio, lo que les permite compartir código. Un ejemplo de un programa de servicio que hace esto es el proceso de host de servicio genérico, Svchost.exe, que hospeda los servicios internos de Windows. Tenga en cuenta que Svchost.exe está reservado para su uso por parte del sistema operativo y no debe ser utilizado por servicios que no sean de Windows. En su lugar, los desarrolladores deben implementar sus propios programas de hospedaje de servicios.

Un programa de servicio se puede configurar para que se ejecute en el contexto de una cuenta de usuario desde el dominio integrado (local), principal o de confianza. También se puede configurar para que se ejecute en una [cuenta de usuario de servicio](service-user-accounts.md)especial.

En los temas siguientes se describen los requisitos de interfaz del [Administrador de control de servicios](service-control-manager.md) (SCM) que un programa de servicio debe incluir:

-   [Punto de entrada de servicio](service-entry-point.md)
-   [Función ServiceMain del servicio](service-servicemain-function.md)
-   [Función de controlador de control de servicio](service-control-handler-function.md)

Estos temas no se aplican a los servicios de controlador. Para conocer los requisitos de la interfaz de los servicios de controladores, consulte el kit de controladores de Windows (WDK).

Un servicio se ejecuta como un proceso en segundo plano que puede afectar al rendimiento del sistema, la capacidad de respuesta, la eficiencia energética y la seguridad. Para obtener instrucciones sobre la optimización del servicio, consulte [desarrollo de procesos en segundo plano eficaces para Windows](/windows-hardware/drivers/kernel/implementing-power-management). En los temas siguientes se describen consideraciones de programación adicionales:

-   [Transiciones de estado del servicio](service-status-transitions.md)
-   [Recepción de eventos en un servicio](receiving-events-in-a-service.md)
-   [Servicios multiproceso](multithreaded-services.md)
-   [Servicios y el registro](services-and-the-registry.md)
-   [Servicios y unidades redirigidas](services-and-redirected-drives.md)
-   [Eventos de desencadenador de servicio](service-trigger-events.md)

Tenga en cuenta que si el programa de servicio funciona como un servidor RPC, debe usar puntos de conexión dinámicos y autenticación mutua.

 

 
