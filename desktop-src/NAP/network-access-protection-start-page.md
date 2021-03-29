---
title: Protección de acceso a redes
description: 'Nota: la plataforma de protección de acceso a redes no está disponible a partir de la protección de acceso a redes (NAP) de Windows 10 es un conjunto de componentes del sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas.'
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protección de acceso a redes
- Protección de acceso a redes, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775337"
---
# <a name="network-access-protection"></a>Protección de acceso a redes

## <a name="purpose"></a>Propósito

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Protección de acceso a redes (NAP) es un conjunto de componentes del sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas. La plataforma NAP proporciona una manera integrada de evaluar el estado de mantenimiento del sistema de un cliente de red que está intentando conectarse o comunicarse en una red y restringir el acceso del cliente de red hasta que se hayan cumplido los requisitos de la Directiva de mantenimiento.

NAP es una plataforma extensible que proporciona una infraestructura y un conjunto de API para agregar componentes que almacenan, informan, validan y corrigen el estado de mantenimiento del sistema de un equipo. Por sí solo, la plataforma NAP no proporciona componentes para acumular y evaluar los atributos del estado de mantenimiento de un equipo. Otros componentes, conocidos como agentes de mantenimiento del sistema (SHA) y validadores de mantenimiento del sistema (SHV), proporcionan la validación de directivas de red y el cumplimiento de las directivas de red.

## <a name="where-applicable"></a>Donde sea aplicable

NAP está diseñado para ser extensible. Puede interoperar con cualquier software de proveedor que proporcione Sha y SHV o que reconozca su conjunto de API publicado. NAP ayuda a proporcionar una solución para los siguientes escenarios comunes:

-   Compruebe el estado de los equipos portátiles móviles.
-   Asegurarse del estado de los equipos de escritorio.
-   Compruebe el cumplimiento y el estado de los equipos de las oficinas remotas.
-   Determinar el estado de los equipos portátiles que se visitan.
-   Compruebe el cumplimiento y el estado de los equipos domésticos no administrados.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de NAP está diseñada para desarrolladores de C/C++. En el caso de los métodos de cumplimiento NAP, los programadores deben estar familiarizados con los protocolos y tecnologías de red como el servicio de autenticación remota telefónica de usuario (RADIUS), el protocolo de configuración dinámica de host (DHCP), las redes privadas virtuales (VPN), el estándar IEEE 802.1 X para el acceso cableado y inalámbrico, y el protocolo de seguridad de Internet (IPsec).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La plataforma NAP requiere servidores de infraestructura NAP que ejecuten Windows Server 2008 o posterior y clientes NAP que ejecuten Windows XP con Service Pack 3 (SP3), Windows Vista o sistemas operativos posteriores. Para obtener información específica sobre qué sistemas operativos admiten un determinado elemento de programación, consulte las secciones de requisitos de las API de NAP en la documentación de referencia de NAP.

## <a name="in-this-section"></a>En esta sección



| Tema                                         | Descripción                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [Acerca de NAP](about-nap.md)<br/>         | Información general sobre la API de NAP.<br/>                                     |
| [Con NAP](using-nap.md)<br/>         | Ejemplos de uso de la API de NAP.<br/>                                            |
| [Referencia de NAP](nap-reference.md)<br/> | Documentación de interfaces, estructuras y otros elementos de código de NAP.<br/> |



 

 

 





