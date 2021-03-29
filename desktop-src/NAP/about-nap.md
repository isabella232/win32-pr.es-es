---
title: Acerca de NAP
description: Acerca de NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773362"
---
# <a name="about-nap"></a>Acerca de NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La protección de acceso a redes (NAP) está diseñada para ayudar a los administradores a mantener el estado de los equipos de la red, lo que, a su vez, ayuda a mantener la integridad general de la red. No está diseñado para proteger una red de usuarios malintencionados. Por ejemplo, si un equipo tiene todo el software y las configuraciones que requiere la Directiva de acceso a la red, el equipo se considera correcto o compatible y se le concederá el acceso adecuado a la red. NAP no impide que un usuario autorizado con un equipo compatible cargue un programa malintencionado a la red o que se confiere a otro comportamiento inadecuado.

Para proteger el acceso a una red, una infraestructura de red debe proporcionar las siguientes áreas de funcionalidad:

-   Validación de estado: determina si los equipos son compatibles con los requisitos de mantenimiento del sistema.
-   Restricción de red: restringe el acceso a la red o la comunicación de los clientes que no cumplen los requisitos de mantenimiento del sistema.
-   Corrección: proporciona las actualizaciones necesarias para permitir que el equipo corrija el estado de mantenimiento no compatible.
-   Cumplimiento continuo: permite el acceso a la red siempre que el equipo del usuario cumpla los requisitos de la Directiva de mantenimiento.

Windows XP con Service Pack 3 (SP3), Windows Vista y Windows Server 2008 proporcionan métodos de cumplimiento NAP para la configuración de direcciones del Protocolo de configuración dinámica de host (DHCP), conexiones de red privada virtual (VPN) basadas en acceso remoto, conexiones cableadas e inalámbricas de IEEE 802.1 X y comunicaciones basadas en el protocolo de seguridad de Internet (IPsec). Además, la plataforma NAP admite una arquitectura a través de la cual la validación de mantenimiento, la restricción de red, la corrección y el cumplimiento continuo son compatibles con componentes adicionales que pueden proporcionar otros proveedores de software o Microsoft.

La plataforma NAP incluye los siguientes componentes:

-   [Arquitectura de cliente de NAP](nap-client-architecture.md)
-   [Arquitectura del lado servidor NAP](nap-server-side-architecture.md)
-   [Comunicación de componentes del lado servidor y del cliente NAP](nap-client-and-server-side-component-communication.md)

El cliente NAP requiere Windows Vista, Windows XP con SP3 o Windows Server 2008. El servidor de directivas de mantenimiento de NAP y los puntos de cumplimiento NAP para DHCP, VPN y cumplimiento IPsec requieren Windows Server 2008.

 

 




