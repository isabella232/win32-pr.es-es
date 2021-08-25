---
description: La programación de multidifusión se habilita Windows sockets.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Programación de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0582f9d03cd5614bbe284eb81cdcb40bea8233627564ec2d3603de11fb663e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858165"
---
# <a name="multicast-programming"></a>Programación de multidifusión

La programación de multidifusión se habilita Windows sockets. Windows Sockets habilita las versiones 1 (MLDv1) y 2 (MLDv2) de detección de escucha de multidifusión (MLD) en IPv6 y el Protocolo de administración de grupos de Internet versiones 2 (IGMPv2) y 3 (IGMPv3) mediante el uso de opciones de socket o IOCTLs. En esta sección se describe Windows implementación, se explica cómo habilitar la programación de multidifusión mediante sockets de Windows y se proporcionan ejemplos de programación para ilustrar su uso.

La segunda versión de IGMP, denominada en adelante IGMPv2, permite a los hosts unirse y dejar grupos de multidifusión identificados por una dirección de multidifusión IPv4 en una interfaz de red específica. Windows Sockets permite que una aplicación se una y deje estos grupos en sockets específicos. Sin embargo, un inconveniente de IGMPv2 es que cualquier dirección de origen IPv4 unida al grupo IGMPv2 puede transmitir a todos los miembros, lo que podría desbordar el grupo y hacer que no se pueda usar para las transmisiones que requieren un origen principal, como una estación de radio de Internet. El problema con IGMPv2 es su incapacidad para elegir de forma selectiva una única dirección de origen IPv4 (o incluso algunos orígenes) y su incapacidad para bloquear remitentes (como emisores no deseados o emisores de denegación de servicio) para un grupo de multidifusión determinado. IGMPv3 aborda esas deficiencias.

Con Windows sockets e IGMPv3, las aplicaciones pueden seleccionar una dirección de origen IPv4 de multidifusión determinada y un par de grupos de multidifusión. Además, Windows Sockets permite a los desarrolladores permitir de forma selectiva emisoras adicionales en un par de origen o grupo determinado, o bien permite que las aplicaciones bloqueen emisores específicos. IGMPv3 se admite en Windows Vista y versiones posteriores.

La primera versión de MLD en IPv6, denominada MLDv1, es muy similar a IGMPv2 y sufre las mismas limitaciones. MLDv1 permite a los hosts unirse y dejar grupos de multidifusión identificados por una dirección de multidifusión IPv6 en una interfaz de red específica. Windows Sockets permite que una aplicación se una y deje estos grupos en sockets específicos. Sin embargo, cualquier dirección de origen IPv6 unida al grupo MLDv1 puede transmitir a todos los miembros, lo que podría desbordar el grupo y hacer que no se pueda usar para las transmisiones que requieren un origen principal. El problema con MLDv1 es su incapacidad para elegir de forma selectiva una única dirección de origen IPv6 (o incluso algunos orígenes) y su incapacidad para bloquear remitentes (como emisores no deseados o emisores de denegación de servicio) para un grupo de multidifusión determinado. MLDv2 aborda esas deficiencias.

Con Windows Sockets y MLDv2, las aplicaciones pueden seleccionar una dirección de origen IPv6 de multidifusión determinada y un par de grupos de multidifusión. Además, Windows Sockets permite a los desarrolladores permitir de forma selectiva emisoras adicionales en un par de origen o grupo determinado, o bien permite que las aplicaciones bloqueen emisores específicos. MLDv2 se admite en Windows Vista y versiones posteriores.

Hay dos enfoques que un programador de aplicaciones puede tomar al desarrollar aplicaciones de multidifusión en Windows. El primer enfoque está basado en cambios; Los orígenes de multidifusión se agregan o quitan mediante las opciones de socket, incluso durante el transcurso de la transmisión, según sea necesario. El segundo enfoque se basa en el estado final; Las direcciones de origen y las direcciones incluidas o excluidas se especifican con una IOCTL. Cada enfoque es una práctica válida de multidifusión, pero los desarrolladores pueden encontrar el uso de opciones de socket y el enfoque basado en cambios más intuitivo y flexible.

Esta sección tiene las páginas siguientes: 

| Título de la página                                                                             | Descripción                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD e IGMP mediante Windows sockets](igmp-and-windows-sockets.md)                     | Enumera las opciones de socket de multidifusión disponibles para su Windows sockets mediante un enfoque de programación basada en cambios. Define dos categorías de aplicación de multidifusión. |
| [Comportamiento de las opciones de socket de multidifusión](multicast-socket-option-behavior.md)               | Proporciona una tabla amplia para explicar las implicaciones y los requisitos de llamar a las opciones de socket de multidifusión en un orden determinado.                                                  |
| [Ejemplo de programación de multidifusión](multicast-programming-sample.md)                       | Fragmento de código de programación que muestra cómo usar las opciones de socket para habilitar aplicaciones de multidifusión en Windows.                                                                        |
| [Programación de multidifusión basada en estado final](final-state-based-multicast-programming.md) | Explica el enfoque de estado final y cómo usar ioCTL para la programación de multidifusión con Windows sockets.                                                                               |
| [Porte de aplicaciones de difusión a IPv6](porting-broadcast-applications-to-ipv6.md)   | Proporciona instrucciones para portear aplicaciones de difusión IPv4 a multidifusión IPv6.                                                                                                     |



 

 

 



