---
title: Introducción a la arquitectura de UPnP
description: La arquitectura UPnP define la conectividad de red punto a punto de dispositivos inteligentes, dispositivos y puntos de control.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5866d3e701f53e95225538655ca45d159fb7c5f67d00e3c46c97357c7a9ee6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126473"
---
# <a name="overview-of-upnp-architecture"></a>Introducción a la arquitectura de UPnP

La arquitectura de UPnP define la conectividad de red punto a punto de dispositivos inteligentes, dispositivos y [*puntos de control*](c-gly.md). Está diseñado para ofrecer conectividad fácil de usar, flexible y basada en estándares a redes ad hoc, administradas o no administradas, independientemente de si estas redes están en el hogar, pequeñas empresas o conectadas directamente a Internet. La arquitectura UPnP es una arquitectura de red distribuida y abierta que usa tecnologías TCP/IP y web existentes para permitir redes de proximidad sin problemas, además de controlar y transferir datos entre dispositivos en red.

UPnP es un conjunto de protocolos basado en IP basado en versiones preliminares de protocolos de servicios Web como XML y Protocolo simple de acceso a objetos (SOAP). Con UPnP, un dispositivo puede unirse dinámicamente a una red, obtener una dirección IP, transmitir su funcionalidad y detectar la presencia y funcionalidades de otros dispositivos en la red.

Un dispositivo UPnP es un contenedor de servicios y dispositivos anidados. Por ejemplo, un VCR podría constar de un servicio de transporte de cintas, un servicio de afinador y un servicio de reloj. Las distintas categorías de dispositivos UPnP están asociadas a diferentes conjuntos de servicios y dispositivos incrustados. Por ejemplo, los servicios dentro de un VCR son diferentes de los de una impresora. La información sobre el conjunto de servicios que un tipo de dispositivo determinado puede proporcionar se captura en un documento de descripción del dispositivo XML que hospeda el dispositivo. La descripción del dispositivo también muestra propiedades como el nombre del dispositivo y los iconos asociados al dispositivo. Microsoft ha mejorado la compatibilidad con UPnP para incluir la integración [con PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x) y [la detección de funciones.](/previous-versions/windows/desktop/fundisc/fd-portal)

La arquitectura de UPnP es algo más que una extensión sencilla del modelo periférico plug-and-play. Admite la configuración cero, redes invisibles y detección automática para una variedad de categorías de dispositivos de una amplia gama de proveedores. Esto permite que un dispositivo se una dinámicamente a una red, obtenga una dirección IP y transmita sus funcionalidades a petición. A continuación, otros puntos de control pueden usar la API de punto de control con tecnología UPnP para obtener información sobre la presencia y las funcionalidades de otros dispositivos. Un dispositivo puede salir de una red sin problemas y automáticamente cuando ya no esté en uso.

¿Qué es universal sobre la tecnología UPnP?

-   Independencia de dispositivos y medios. La tecnología UPnP se puede ejecutar en cualquier medio, incluida la línea de teléfono, la línea de alimentación, Ethernet, radiofrecuencia y 1394.
-   Independencia de la plataforma. Los proveedores usan cualquier sistema operativo y cualquier lenguaje de programación para crear productos basados en UPnP.
-   Tecnologías basadas en Internet. La tecnología UPnP se basa en IP, TCP, UDP, HTTP y XML, entre otros.
-   Control de interfaz de usuario. La arquitectura UPnP permite al proveedor controlar la interfaz de usuario del dispositivo y la interacción mediante el explorador.
-   Control mediante programación. La arquitectura UPnP también habilita el control de programación de aplicaciones convencionales.
-   Protocolos base comunes. Los proveedores están de acuerdo en los conjuntos de protocolos base por dispositivo.
-   Extensible. Cada producto basado en UPnP puede tener servicios de valor añadido por encima de la arquitectura básica de dispositivos por parte de los fabricantes individuales.

La tecnología UPnP tiene un ámbito amplio, ya que tiene como destino redes de hogar, redes de proximidad y redes en pequeñas empresas y edificios comerciales. Permite la comunicación de datos entre dos dispositivos cualquiera bajo el comando de cualquier dispositivo de control de la red. La tecnología UPnP es independiente de cualquier sistema operativo, lenguaje de programación o medio físico determinado.

Microsoft proporciona dos API para trabajar con dispositivos basados en UPnP:

-   [API de punto de](control-point-api.md) control: proporciona un conjunto de interfaces COM que permiten a las aplicaciones buscar y controlar dispositivos basados en UPnP.
-   [API de host de](device-host-api.md) dispositivo: proporciona un conjunto de interfaces COM que permiten a los desarrolladores escribir la funcionalidad básica del dispositivo y registrar el dispositivo en el host de dispositivo. El host de dispositivo controla las partes de detección, descripción, control y eventos de la funcionalidad del dispositivo basada en UPnP.

 

 