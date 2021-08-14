---
title: Protocolo de enrutamiento
description: Un protocolo de enrutamiento es un tipo de cliente que se registra con el administrador de tablas de enrutamiento. Los enrutadores usan protocolos de enrutamiento para intercambiar información relacionada con las rutas a un destino.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 879d540662db7d1a1603bf40818101d0e7f9cb6988d4c0065f922fdc8f73e381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977848"
---
# <a name="routing-protocol"></a>Protocolo de enrutamiento

Un protocolo de enrutamiento es un tipo de cliente que se registra con el administrador de tablas de enrutamiento. Los enrutadores usan protocolos de enrutamiento para intercambiar información relacionada con las rutas a un destino.

Los protocolos de enrutamiento son unidifusión o multidifusión. Los protocolos de enrutamiento anuncian rutas a un destino.

Un protocolo de enrutamiento de unidifusión usa una ruta de unidifusión a un destino para reenviar datos de unidifusión a ese destino. Algunos ejemplos de protocolos de enrutamiento de unidifusión son: Protocolo de información de enrutamiento (RIP), Open Shortest Path First (OSPF) y Protocolo de puerta de enlace de borde (BGP).

Algunos protocolos de enrutamiento de multidifusión usan una ruta de multidifusión a un destino para crear la información que se usa para reenviar datos de multidifusión desde hosts en la red de destino de la ruta (lo que se conoce como reenvío de ruta inversa). Algunos ejemplos de protocolos de enrutamiento de multidifusión son: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP) y Protocol Independent Multicast (PIM).

El administrador de tablas de enrutamiento admite varias instancias del mismo protocolo (como la implementación de Microsoft de OSPF y un OSPF de terceros) que se ejecutan en el enrutador. Esto permite a los enrutadores usar las distintas funcionalidades de cada versión. Estos protocolos tienen identificadores de protocolo diferentes.

Los identificadores de protocolo se componen de un identificador de proveedor y un identificador específico del protocolo. El identificador específico del protocolo es el mismo para las distintas implementaciones del protocolo, como la implementación de OSPF de Microsoft y una implementación de terceros de OSPF. Solo cuando se combinan los identificadores específicos del proveedor y del protocolo, hay un identificador único para un protocolo de enrutamiento.

Un protocolo con el mismo identificador de protocolo (es decir, el mismo identificador de proveedor y el mismo identificador específico del protocolo) puede registrarse varias veces con el administrador de tablas de enrutamiento. Cada vez, el protocolo se registra mediante un identificador de instancia de protocolo diferente. Por ejemplo, una implementación de OSPF de un proveedor determinado puede registrarse como Vendor-OSPF-1 y Vendor-OSPF-2. Esto permite que una implementación de protocolo específica particionar la información que mantiene en la tabla de enrutamiento.

 

 




