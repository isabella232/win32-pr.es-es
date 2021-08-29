---
title: Acerca de NAP
description: Acerca de NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fcf0b653ae72dcae4bd62958b9b85e238af3e421b9ae18bb9faf58a2faa4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891735"
---
# <a name="about-nap"></a>Acerca de NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Protección de acceso a redes (NAP) está diseñado para ayudar a los administradores a mantener el estado de los equipos de la red, lo que a su vez ayuda a mantener la integridad general de la red. No está diseñado para proteger una red de usuarios malintencionados. Por ejemplo, si un equipo tiene todo el software y las configuraciones que requiere la directiva de acceso a la red, el equipo se considera correcto o compatible y se le concederá el acceso adecuado a la red. NAP no impide que un usuario autorizado con un equipo compatible cargue un programa malintencionado en la red o se dedúe a otros comportamientos inadecuados.

Para proteger el acceso a una red, una infraestructura de red debe proporcionar las siguientes áreas de funcionalidad:

-   Validación de estado: determina si los equipos son compatibles con los requisitos de mantenimiento del sistema.
-   Restricción de red: restringe el acceso a la red o la comunicación para los clientes que no cumplen los requisitos de mantenimiento del sistema.
-   Corrección: proporciona las actualizaciones necesarias para permitir que el equipo corrija su estado de mantenimiento no conforme.
-   Cumplimiento continuo: permite el acceso a la red siempre que el equipo del usuario cumpla los requisitos de la directiva de mantenimiento.

Windows XP con Service Pack 3 (SP3), Windows Vista y Windows Server 2008 proporcionan métodos de cumplimiento de NAP para la configuración de direcciones del Protocolo de configuración dinámica de host (DHCP), las conexiones de red privada virtual (VPN) basadas en acceso remoto, las conexiones cableadas e inalámbricas autenticadas por IEEE 802.1X y las comunicaciones basadas en la seguridad del protocolo de Internet (IPsec). La plataforma NAP admite además una arquitectura a través de la cual la validación de estado, la restricción de red, la corrección y el cumplimiento continuo son compatibles con componentes adicionales que pueden proporcionar proveedores de software de terceros o Microsoft.

La plataforma NAP incluye los siguientes componentes:

-   [Arquitectura de cliente NAP](nap-client-architecture.md)
-   [Arquitectura del lado servidor NAP](nap-server-side-architecture.md)
-   [Comunicación de cliente NAP y componente del lado servidor](nap-client-and-server-side-component-communication.md)

El cliente NAP requiere Windows Vista, Windows XP con SP3 o Windows Server 2008. El servidor de directivas de mantenimiento de NAP y los puntos de cumplimiento de NAP para el cumplimiento de DHCP, VPN e IPsec requieren Windows Server 2008.

 

 




