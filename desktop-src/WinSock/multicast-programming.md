---
description: La programación multidifusión se habilita a través de Windows Sockets.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Programación multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67af0eeb087e8c6a5938f26a0644dc346d55cf51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541563"
---
# <a name="multicast-programming"></a>Programación multidifusión

La programación multidifusión se habilita a través de Windows Sockets. Windows Sockets habilita las versiones 1 (MLDv1) y 2 (MLDv2) de detección de escucha de multidifusión (MLD) en IPv6 y el protocolo de administración de grupos de Internet versiones 2 (IGMPv2) y 3 (IGMPv3) mediante el uso de opciones de socket o ioctl. En esta sección se describe la implementación de Windows, se explica cómo habilitar la programación multidifusión con Windows Sockets y se proporcionan ejemplos de programación para ilustrar su uso.

La segunda versión de IGMP, que ahora se conoce como IGMPv2, permite a los hosts unir y dejar grupos de multidifusión identificados mediante una dirección de multidifusión IPv4 en una interfaz de red específica. Windows Sockets permite a una aplicación combinar y dejar estos grupos en sockets específicos. Sin embargo, un inconveniente de IGMPv2 es que cualquier dirección de origen IPv4 unida al grupo IGMPv2 se puede transmitir a todos los miembros, lo que podría inundar el grupo y hacer que quede inutilizable para las transmisiones que requieren un origen principal, como una emisora de radio por Internet. El problema con IGMPv2 es su incapacidad para elegir de forma selectiva una única dirección de origen IPv4 (o incluso unos pocos orígenes) y su incapacidad para bloquear a los remitentes (por ejemplo, los emisores no autorizados o los autores de denegación de servicio) de un grupo de multidifusión determinado. IGMPv3 aborda esas deficiencias.

Con Windows Sockets y IGMPv3, las aplicaciones pueden seleccionar una dirección de origen IPv4 de multidifusión y un par de grupos de multidifusión determinados. Además, Windows Sockets permite a los desarrolladores permitir selectivamente emisores adicionales en un par de origen y grupo determinado, o bien permite a las aplicaciones bloquear emisores específicos. IGMPv3 es compatible con Windows Vista y versiones posteriores.

La primera versión de MLD en IPv6, denominada MLDv1, es muy similar a IGMPv2 y se ve afectada por las mismas limitaciones. MLDv1 permite a los hosts unir y dejar grupos de multidifusión identificados por una dirección IPv6 de multidifusión en una interfaz de red específica. Windows Sockets permite a una aplicación combinar y dejar estos grupos en sockets específicos. Sin embargo, cualquier dirección de origen IPv6 unida al grupo MLDv1 se puede transmitir a todos los miembros, lo que podría inundar el grupo y hacer que quede inutilizable para las transmisiones que requieran un origen principal. El problema con MLDv1 es su incapacidad para elegir de forma selectiva una única dirección de origen IPv6 (o incluso unos pocos orígenes) y su incapacidad para bloquear a los remitentes (por ejemplo, emisores no autorizados o autores de denegación de servicio) de un grupo de multidifusión determinado. MLDv2 aborda esas deficiencias.

Con Windows Sockets y MLDv2, las aplicaciones pueden seleccionar una dirección de origen IPv6 de multidifusión y un par de grupos de multidifusión determinados. Además, Windows Sockets permite a los desarrolladores permitir selectivamente emisores adicionales en un par de origen y grupo determinado, o bien permite a las aplicaciones bloquear emisores específicos. MLDv2 es compatible con Windows Vista y versiones posteriores.

Existen dos enfoques que puede realizar un programador de aplicaciones al desarrollar aplicaciones de multidifusión en Windows. El primer enfoque se basa en cambios; los orígenes de multidifusión se agregan o se quitan mediante las opciones de socket, incluso durante el transcurso de la transmisión, según sea necesario. El segundo enfoque es basado en el estado final; las direcciones de origen y cualquier dirección incluida/excluida se especifican con un IOCTL. Cada enfoque es una práctica de multidifusión válida, pero los desarrolladores pueden encontrar opciones de socket y el enfoque basado en cambios es más intuitivo y flexible.

Esta sección contiene las siguientes páginas: 

| Título de la página                                                                             | Descripción                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD y IGMP con Windows Sockets](igmp-and-windows-sockets.md)                     | Enumera las opciones de socket de multidifusión disponibles para su uso en la programación de Windows Sockets, mediante un enfoque de programación basado en cambios. Define dos categorías de aplicaciones de multidifusión. |
| [Comportamiento de la opción de socket de multidifusión](multicast-socket-option-behavior.md)               | Proporciona una tabla extensa para explicar las implicaciones y los requisitos de llamar a las opciones de socket de multidifusión en un orden determinado.                                                  |
| [Ejemplo de programación de multidifusión](multicast-programming-sample.md)                       | Fragmento de código de programación que muestra cómo usar las opciones de socket para habilitar las aplicaciones de multidifusión en Windows.                                                                        |
| [Programación de multidifusión basada en el estado final](final-state-based-multicast-programming.md) | Explica el enfoque de estado final y cómo usar ioctl para la programación multidifusión con Windows Sockets.                                                                               |
| [Trasladar aplicaciones de difusión a IPv6](porting-broadcast-applications-to-ipv6.md)   | Proporciona directrices para trasladar aplicaciones IPv4 de difusión a multidifusión de IPv6.                                                                                                     |



 

 

 



