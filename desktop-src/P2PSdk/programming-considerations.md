---
description: En este tema se de abordan consideraciones de programación específicas al usar la infraestructura del mismo nivel.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Consideraciones de programación (punto a punto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d5af967503c216422e3a12572aeeaf91d751473f88d8589c2e125894721b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518065"
---
# <a name="programming-considerations-peer-to-peer"></a>Consideraciones de programación (punto a punto)

En este tema se de abordan consideraciones de programación específicas al usar la infraestructura del mismo nivel.

Al usar la infraestructura del mismo nivel para desarrollar aplicaciones del mismo nivel, debe tener en cuenta las siguientes consideraciones de programación:

-   IPv6

    La infraestructura del mismo nivel requiere que IPv6 esté instalado e iniciado para permitir que las aplicaciones de red del mismo nivel funcionen.

-   Puertos de firewall

    Cuando se usa un firewall en una red (como el firewall de conexión a Internet IPv6), se deben abrir puertos específicos para permitir que la infraestructura del mismo nivel funcione. Los siguientes puertos deben estar abiertos:

    Puerto TCP 3587 para la infraestructura de agrupación del mismo nivel.

    Puerto UDP 3540 para la infraestructura de grafos del mismo nivel.

    > [!Note]  
    > Las aplicaciones que usan la infraestructura de grafos del mismo nivel a través de TCP eligen su propio puerto TCP al llamar a [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Opción de socket

    Al intentar conectarse directamente a otros nodos del mismo nivel IPv6 (sin usar la infraestructura del mismo nivel), asegúrese de que la opción de socket IPV6 PROTECTION LEVEL esté establecida en \_ \_ PROTECTION LEVEL **\_ \_ UNRESTRICTED**.

-   Ancho de banda

    Cuando se usa PNRP, una aplicación puede publicar uno o [varios](peer-names.md) nombres del mismo nivel que se puedan resolver. Para cada nombre del mismo nivel registrado con PNRP, hay un aumento en el ancho de banda de red que usa PNRP para publicar el nombre del mismo nivel y mantenerlo disponible para que lo resuelvan otros nodos.

    Para evitar el uso de demasiado ancho de banda, las aplicaciones deben evitar el registro de un gran número de nombres del mismo nivel en un equipo. Por ejemplo, una aplicación que publica imágenes no debe crear un nombre del mismo nivel para cada imagen, sino que debe crear un nombre del mismo nivel para el servicio que publica imágenes y usar un protocolo diferente para que los clientes consulten el servicio para imágenes específicas.

-   Registro de nombres del mismo nivel

    Es posible que algunas aplicaciones deba registrar el [mismo](peer-names.md) nombre del mismo nivel en más de un equipo. Normalmente, esto sucede si un nombre del mismo nivel está asociado a una persona que usa más de un equipo. Un método que puede usar para registrar el mismo nombre del mismo nivel en varios equipos es crear un grupo del mismo nivel para la persona y conectarse a ese grupo desde todos los equipos. Otro método consiste en crear una identidad del mismo nivel y un nombre del mismo nivel en un equipo, exportar la identidad del mismo nivel desde ese equipo e importarla en otros equipos. Esto permite crear el mismo nombre seguro del mismo nivel en todos los equipos que han importado la identidad del mismo nivel.

 

 



