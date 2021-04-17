---
description: En este tema se tratan las consideraciones de programación específicas al usar la infraestructura del mismo nivel.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Consideraciones de programación (punto a punto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667385"
---
# <a name="programming-considerations-peer-to-peer"></a>Consideraciones de programación (punto a punto)

En este tema se tratan las consideraciones de programación específicas al usar la infraestructura del mismo nivel.

Al usar la infraestructura del mismo nivel para desarrollar aplicaciones del mismo nivel, debe tener en cuenta las siguientes consideraciones de programación:

-   IPv6

    La infraestructura del mismo nivel requiere que IPv6 esté instalado e iniciado para permitir que funcionen las aplicaciones de redes del mismo nivel.

-   Puertos de Firewall

    Cuando se usa un firewall en una red (como el Firewall de conexión a Internet IPv6), se deben abrir puertos específicos para permitir que la infraestructura del mismo nivel funcione. Los siguientes puertos deben estar abiertos:

    Puerto TCP 3587 para la infraestructura de agrupación del mismo nivel.

    Puerto UDP 3540 para la infraestructura de gráficos del mismo nivel.

    > [!Note]  
    > Las aplicaciones que usan la infraestructura de gráficos del mismo nivel en TCP eligen su propio puerto TCP al llamar a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Opción de socket

    Al intentar conectarse a otros nodos IPv6 del mismo nivel directamente (sin usar la infraestructura del mismo nivel), asegúrese de que la opción de socket \_ nivel de protección IPv6 \_ está establecida en **nivel de protección \_ \_ sin restricciones**.

-   Ancho de banda

    Cuando se usa PNRP, una aplicación puede publicar uno o más [nombres del mismo nivel](peer-names.md) que se pueden resolver. Para cada nombre del mismo nivel registrado con PNRP, existe un aumento en el ancho de banda de red que usa PNRP para publicar el nombre del mismo nivel y mantenerlo disponible para ser resuelto por otros nodos.

    Para evitar el uso de demasiado ancho de banda, las aplicaciones deben evitar el registro de un gran número de nombres de mismo nivel en un equipo. Por ejemplo, una aplicación que publica imágenes no debe crear un nombre de mismo nivel para cada imagen, sino que debe crear un nombre del mismo nivel para el servicio que publica imágenes, y usar un protocolo diferente para que los clientes consulten imágenes específicas en el servicio.

-   Registro de nombre del mismo nivel

    Es posible que se necesiten algunas aplicaciones para registrar el mismo [nombre del mismo nivel](peer-names.md) en más de un equipo. Normalmente, esto sucede si un nombre del mismo nivel está asociado a una persona que usa más de un equipo. Un método que puede usar para registrar el mismo nombre del mismo nivel en varios equipos es crear un grupo del mismo nivel para la persona y conectarse a ese grupo desde todos los equipos. Otro método consiste en crear una identidad del mismo nivel y el nombre del mismo nivel en un equipo, exportar la identidad del mismo nivel desde ese equipo e importarlo en otros equipos. Esto permite crear el mismo nombre seguro del mismo nivel en todos los equipos que han importado la identidad del mismo nivel.

 

 



