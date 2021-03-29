---
title: Protocolo de enrutamiento
description: Un protocolo de enrutamiento es un tipo de cliente que se registra con el administrador de tablas de enrutamiento. Los enrutadores usan protocolos de enrutamiento para intercambiar información relacionada con las rutas a un destino.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075627"
---
# <a name="routing-protocol"></a>Protocolo de enrutamiento

Un protocolo de enrutamiento es un tipo de cliente que se registra con el administrador de tablas de enrutamiento. Los enrutadores usan protocolos de enrutamiento para intercambiar información relacionada con las rutas a un destino.

Los protocolos de enrutamiento son unidifusión o multidifusión. Los protocolos de enrutamiento anuncian rutas a un destino.

Un protocolo de enrutamiento de unidifusión utiliza una ruta de unidifusión a un destino para reenviar datos de unidifusión a ese destino. Algunos ejemplos de protocolos de enrutamiento de unidifusión son: Protocolo de información de enrutamiento (RIP), ruta de acceso más corta primero (OSPF) y Protocolo de puerta de enlace de borde (BGP).

Algunos protocolos de enrutamiento de multidifusión utilizan una ruta de multidifusión a un destino para crear la información que se usa para reenviar datos de multidifusión desde hosts de la red de destino de la ruta (lo que se conoce como reenvío de ruta de acceso inversa). Entre los ejemplos de protocolos de enrutamiento de multidifusión se incluyen: ruta de acceso más corta de apertura de multidifusión primero (MOSPF), protocolo de enrutamiento de multidifusión del vector de distancia (DVMRP) y multidifusión independiente del Protocolo (PIM).

El administrador de tabla de enrutamiento admite varias instancias del mismo protocolo (como la implementación de Microsoft de OSPF y un OSPF de terceros) que se ejecutan en el enrutador. Esto permite a los enrutadores usar las diferentes capacidades de cada versión. Estos protocolos tienen diferentes identificadores de protocolo.

Los identificadores de protocolo se componen de un identificador de proveedor y un identificador específico del protocolo. El identificador específico del protocolo es el mismo para las distintas implementaciones del Protocolo, como la implementación de Microsoft de OSPF y una implementación de terceros de OSPF. Solo cuando los identificadores de proveedor y específicos de protocolo se combinan, existe un identificador único para un protocolo de enrutamiento.

Un protocolo con el mismo identificador de protocolo (es decir, el mismo identificador de proveedor e identificador específico del Protocolo) se puede registrar varias veces en el administrador de tablas de enrutamiento. Cada vez, el protocolo se registra mediante un identificador de instancia de protocolo diferente. Por ejemplo, una implementación de OSPF de un proveedor determinado puede registrarse como proveedor-OSPF-1 y proveedor-OSPF-2. Esto permite que una implementación de protocolo específica divida la información que mantiene en la tabla de enrutamiento.

 

 




