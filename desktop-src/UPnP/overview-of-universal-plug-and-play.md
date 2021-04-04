---
title: Información general sobre la arquitectura de UPnP
description: La arquitectura de UPnP define la conectividad de red punto a punto de dispositivos, dispositivos y puntos de control inteligentes.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ce11009bfecfe03fa176c1e6c75be173fbde86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904741"
---
# <a name="overview-of-upnp-architecture"></a>Información general sobre la arquitectura de UPnP

La arquitectura de UPnP define la conectividad de red punto a punto de dispositivos, dispositivos y [*puntos de control*](c-gly.md)inteligentes. Está diseñado para ofrecer una conectividad fácil de usar, flexible y basada en estándares a redes ad hoc, administradas o no administradas, tanto si estas redes están en casa, pequeñas como si están conectadas directamente a Internet. La arquitectura de UPnP es una arquitectura de red distribuida y abierta que usa las tecnologías TCP/IP y Web existentes para habilitar redes de proximidad sin problemas, además de control y transferencia de datos entre dispositivos en red.

UPnP es un conjunto de protocolos basado en IP basado en las versiones preliminares de los protocolos de servicios web como XML y el Protocolo simple de acceso a objetos (SOAP). Con UPnP, un dispositivo puede unirse dinámicamente a una red, obtener una dirección IP, transmitir su capacidad y detectar la presencia y las capacidades de otros dispositivos en la red.

Un dispositivo UPnP es un contenedor de servicios y dispositivos anidados. Por ejemplo, un VCR puede consistir en un servicio de transporte de cinta, un servicio de sintonizador y un servicio de reloj. Las distintas categorías de dispositivos UPnP están asociadas a diferentes conjuntos de servicios y dispositivos incrustados. Por ejemplo, los servicios de un VCR son diferentes de los de una impresora. La información sobre el conjunto de servicios que un determinado tipo de dispositivo puede proporcionar se captura en un documento de descripción de dispositivo XML que el dispositivo hospeda. La descripción del dispositivo también muestra propiedades como el nombre del dispositivo y los iconos asociados al dispositivo. Microsoft ha mejorado la compatibilidad con UPnP para incluir [la integración con PnP-X y la detección de](/previous-versions/windows/desktop/fundisc/pnp-x) [funciones](/previous-versions/windows/desktop/fundisc/fd-portal).

La arquitectura de UPnP es algo más que una simple extensión del modelo periférico de plug and Play. Admite la red invisible y la detección automática para una variedad de categorías de dispositivos de una amplia variedad de proveedores. Esto permite a un dispositivo unirse dinámicamente a una red, obtener una dirección IP y transmitir sus capacidades a petición. Después, otros puntos de control pueden usar la API de punto de control con tecnología UPnP para obtener información sobre la presencia y las capacidades de otros dispositivos. Un dispositivo puede dejar una red sin problemas y automáticamente cuando ya no está en uso.

¿Qué es universal sobre la tecnología UPnP?

-   Independencia de medios y dispositivos. La tecnología UPnP puede ejecutarse en cualquier medio, como una línea telefónica, una línea de alimentación, Ethernet, RF y 1394.
-   Independencia de la plataforma. Los proveedores utilizan cualquier sistema operativo y cualquier lenguaje de programación para compilar productos basados en UPnP.
-   Tecnologías basadas en Internet. La tecnología UPnP se basa en IP, TCP, UDP, HTTP y XML, entre otros.
-   Control de IU. La arquitectura UPnP permite el control del proveedor sobre la interfaz de usuario del dispositivo y la interacción con el explorador.
-   Control mediante programación. La arquitectura UPnP también habilita el control de programación de aplicaciones convencionales.
-   Protocolos base comunes. Los proveedores acuerdan los conjuntos de protocolos base en cada dispositivo.
-   Ampliable. Cada producto basado en UPnP puede tener servicios de valor añadido superpuestos en la arquitectura de dispositivo básica por parte de los fabricantes individuales.

La tecnología UPnP tiene un ámbito amplio en el sentido de que se dirige a redes domésticas, redes de proximidad y redes en pequeñas empresas y edificios comerciales. Permite la comunicación de datos entre dos dispositivos cualesquiera en el comando de cualquier dispositivo de control de la red. La tecnología UPnP es independiente de cualquier sistema operativo, lenguaje de programación o medio físico en particular.

Microsoft proporciona dos API para trabajar con dispositivos basados en UPnP:

-   [API de punto de control](control-point-api.md) : proporciona un conjunto de interfaces com que permiten a las aplicaciones buscar y controlar dispositivos basados en UPnP.
-   [API de host de dispositivo](device-host-api.md) : proporciona un conjunto de interfaces com que permiten a los desarrolladores escribir la funcionalidad básica del dispositivo y registrar el dispositivo con el host del dispositivo. El host de dispositivo controla las partes de detección, descripción, control y eventos de la funcionalidad de dispositivos basados en UPnP.

 

 