---
title: Tablas de rutas y entradas de tabla de rutas
description: El administrador de tablas de enrutamiento mantiene tablas de rutas distintas para cada familia de protocolos.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31fea4ac965fe397d5bb7eba2b65479358a1e192f1583b1e7e73c2532dbd3a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788060"
---
# <a name="route-tables-and-route-table-entries"></a>Tablas de rutas y entradas de tabla de rutas

**Windows Server 2003:** Esta API ha sido reemplazada por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las nuevas aplicaciones deben usar la API de Routing Table Manager versión 2.

El administrador de tablas de enrutamiento mantiene tablas de rutas distintas para cada familia de protocolos. Actualmente, se proporciona compatibilidad explícita para las familias de protocolos de enrutamiento de Protocolo de Internet (IP) e Internet Packet Exchange (IPX). Independientemente de la familia de protocolos, cada entrada de ruta contiene la siguiente información:

-   Red de destino.
-   Identificador del protocolo que agregó la ruta.
-   Índice de la interfaz a través de la que se obtuvo la ruta. Este valor de índice es el valor numérico asignado a una interfaz de red (basada en hardware o virtual) que transmite los datos a la red. (Por ejemplo, una NIC Ethernet o una tarjeta inalámbrica 802.1b).
-   Dirección del enrutador del próximo salto. RRAS usa este enrutador para reenviar paquetes a la red de destino si la red no está conectada directamente.
-   Hora en que se creó o actualizó por última vez la ruta.
-   Cantidad de tiempo que esta ruta se mantiene en la tabla de enrutamiento. Si transcurre esta cantidad de tiempo y la ruta no se ha actualizado, el administrador de tablas de enrutamiento quita la ruta de la tabla. En este caso, se dice que la ruta ha *pasado a ser .*
-   Datos específicos de la familia de protocolos. Estos datos son transparentes para RTMv1. Sin embargo, si estos datos cambian para una ruta designada como "mejor ruta", el administrador de tablas de enrutamiento envía una notificación de cambio de ruta.
-   Datos específicos del protocolo de enrutamiento. Estos datos son completamente transparentes para el administrador de tablas de enrutamiento, ya que los cambios en estos datos no provocan una notificación de cambio de ruta.

Los siguientes valores tomados juntos identifican de forma única una ruta en la tabla de enrutamiento:

-   Red de destino
-   Identificador de protocolo
-   Índice de interfaz
-   Dirección del enrutador de próximo salto

En general, el administrador de tablas de enrutamiento crea entradas independientes para las rutas que difieren en cualquiera de estos valores de parámetro. Sin embargo, se realiza una excepción para los protocolos de enrutamiento que no mantienen más de una entrada para cada red de destino. Para estos protocolos, el administrador de tablas de enrutamiento omite las diferencias en el índice de interfaz o la dirección del próximo salto. Un ejemplo de este tipo de protocolo es la implementación de RRAS de Open Shortest Path First (OSPF).

 

 




