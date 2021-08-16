---
title: Protección de acceso a redes
description: Nota La plataforma de protección de acceso a redes no está disponible a partir de Windows 10 Network Access Protection (NAP) es un conjunto de componentes de sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protección de acceso a redes
- Protección de acceso a la red, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e5b5121566c3626ee7a9f2ba5d85efc1bf6cff17b412cd99874ae9b346780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939133"
---
# <a name="network-access-protection"></a>Protección de acceso a redes

## <a name="purpose"></a>Propósito

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Protección de acceso a redes (NAP) es un conjunto de componentes de sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas. La plataforma NAP proporciona una manera integrada de evaluar el estado de mantenimiento del sistema de un cliente de red que intenta conectarse o comunicarse en una red y restringir el acceso del cliente de red hasta que se cumplen los requisitos de la directiva de mantenimiento.

NAP es una plataforma extensible que proporciona una infraestructura y un conjunto de API para agregar componentes que almacenan, informan, validan y corrigen el estado de mantenimiento del sistema de un equipo. Por sí misma, la plataforma NAP no proporciona componentes para acumular y evaluar atributos del estado de mantenimiento de un equipo. Otros componentes, conocidos como agentes de mantenimiento del sistema (SHA) y validadores de estado del sistema (SHV), proporcionan validación de directivas de red y cumplimiento de directivas de red.

## <a name="where-applicable"></a>Donde sea aplicable

NAP está diseñado para ser extensible. Puede interoperar con cualquier software de proveedor que proporciona SHAs y SHV o que reconoce su conjunto de API publicado. NAP ayuda a proporcionar una solución para los siguientes escenarios comunes:

-   Compruebe el estado y el estado de los equipos portátiles móviles.
-   Garantizar el estado de los equipos de escritorio.
-   Compruebe el cumplimiento y el estado de los equipos en oficinas remotas.
-   Determine el estado de los portátiles que visitan.
-   Compruebe el cumplimiento y el estado de los equipos no administrados en el hogar.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API nap está diseñada para desarrolladores de C/C++. Para los métodos de aplicación de NAP, los programadores deben estar familiarizados con los protocolos de red y las tecnologías, como el servicio de usuario de acceso telefónico de autenticación remota (RADIUS), el protocolo de configuración dinámica de host (DHCP), las redes privadas virtuales (VPN), el estándar IEEE 802.1X para el acceso cableado e inalámbrico y la seguridad del protocolo de Internet (IPsec).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La plataforma NAP requiere servidores de infraestructura NAP que ejecuten Windows Server 2008 o posterior y clientes NAP que ejecuten Windows XP con Service Pack 3 (SP3), Windows Vista o sistemas operativos posteriores. Para obtener información específica sobre qué sistemas operativos admiten un elemento de programación determinado, consulte las secciones Requisitos de las API de NAP en la documentación de referencia de NAP.

## <a name="in-this-section"></a>En esta sección



| Tema                                         | Descripción                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [Acerca de NAP](about-nap.md)<br/>         | Información general sobre la API de NAP.<br/>                                     |
| [Con NAP](using-nap.md)<br/>         | Ejemplos de uso de la API de NAP.<br/>                                            |
| [Referencia de NAP](nap-reference.md)<br/> | Documentación de interfaces, estructuras y otros elementos de código de NAP.<br/> |



 

 

 





