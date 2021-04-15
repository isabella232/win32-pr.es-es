---
title: Tablas de rutas y entradas de tabla de rutas
description: El administrador de tablas de enrutamiento mantiene distintas tablas de rutas para cada familia de protocolos.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f118ec1d0a6f8fe4ef301654e139f217257c3a0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676099"
---
# <a name="route-tables-and-route-table-entries"></a>Tablas de rutas y entradas de tabla de rutas

**Windows Server 2003:** Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las nuevas aplicaciones deben usar la API del administrador de tablas de enrutamiento versión 2.

El administrador de tablas de enrutamiento mantiene distintas tablas de rutas para cada familia de protocolos. Actualmente, se proporciona compatibilidad explícita para las familias del Protocolo de Internet (IP) y del Protocolo de enrutamiento de intercambio de paquetes de Internet (IPX). Independientemente de la familia de protocolos, cada entrada de ruta contiene la siguiente información:

-   Red de destino.
-   Identificador del protocolo que agregó la ruta.
-   Índice de la interfaz a través de la cual se obtuvo la ruta. Este valor de índice es el valor numérico asignado a una interfaz de red (basada en hardware o virtual) que transmite los datos a la red. (Por ejemplo, una NIC Ethernet o una tarjeta inalámbrica 802.1 b).
-   Dirección del enrutador del próximo salto. RRAS usa este enrutador para reenviar paquetes a la red de destino si la red no está conectada directamente.
-   La hora en que se creó o actualizó por última vez la ruta.
-   Cantidad de tiempo que esta ruta se mantiene en la tabla de enrutamiento. Si esta cantidad de tiempo transcurre y la ruta no se ha actualizado, el administrador de tablas de enrutamiento quita la ruta de la tabla. En este caso, se dice que la ruta ha *vencido*.
-   Datos específicos de la familia de protocolos. Estos datos son transparentes para RTMv1. Sin embargo, si estos datos cambian para una ruta designada como "mejor ruta", el administrador de tablas de enrutamiento envía una notificación de cambio de ruta.
-   Datos específicos del Protocolo de enrutamiento. Estos datos son completamente transparentes para el administrador de tablas de enrutamiento; en ese cambio, los cambios en estos datos no causan la notificación de cambio de ruta.

Los siguientes valores se han tomado juntos de forma única en la tabla de enrutamiento:

-   Red de destino
-   Identificador de protocolo
-   Índice de interfaz
-   Dirección del enrutador de próximo salto

En general, el administrador de tablas de enrutamiento crea entradas independientes para las rutas que difieren en cualquiera de estos valores de parámetro. Sin embargo, se realiza una excepción para los protocolos de enrutamiento que no conservan más de una entrada para cada red de destino. Para estos protocolos, el administrador de tablas de enrutamiento omite las diferencias en el índice de interfaz o en la dirección de próximo salto. Un ejemplo de este tipo de protocolo es la implementación de RRAS de la ruta de acceso más corta abierta primero (OSPF).

 

 




