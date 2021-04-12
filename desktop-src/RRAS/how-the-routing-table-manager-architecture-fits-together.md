---
title: Cómo encaja la arquitectura del administrador de tablas de enrutamiento
description: En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357791"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Cómo encaja la arquitectura del administrador de tablas de enrutamiento

En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.

![relación entre los componentes del enrutador](images/rtsrvarch.png)

Cuando se arranca el enrutador, se inicia el servicio Administrador de enrutadores, así como uno o más protocolos de enrutamiento. Los protocolos de enrutamiento están asociados a las diversas interfaces en el enrutador. El administrador de enrutadores también inicia el administrador de tablas de enrutamiento.

En la ilustración siguiente se muestra la relación entre los clientes y los distintos componentes del administrador de tablas de enrutamiento.

![relación entre los clientes y los componentes del administrador de tablas de enrutamiento](images/rtmentrel.png)

El administrador de enrutadores inicia una o varias instancias del administrador de tablas de enrutamiento. Cuando se inician varias instancias del administrador de tablas de enrutamiento, el enrutador se ha configurado para actuar como uno o más enrutadores virtuales. Cada instancia del administrador de tabla de enrutamiento posee una o más interfaces; cada interfaz solo puede ser propiedad de una instancia del administrador de tablas de enrutamiento.

Cada instancia del administrador de tabla de enrutamiento es independiente de las demás; no se intercambia información entre las instancias.

Cada instancia del administrador de tablas de enrutamiento contiene una o más tablas de enrutamiento. Cada tabla de enrutamiento está asociada a una familia de direcciones.

Cada tabla de enrutamiento contiene una o más vistas. En este ejemplo, la tabla de enrutamiento se muestra con una vista de unidifusión y multidifusión. Cada vista es un subconjunto de la tabla de enrutamiento.

En la ilustración siguiente se muestra la relación entre los clientes y varias instancias del administrador de tablas de enrutamiento, las tablas de enrutamiento y las vistas.

![clientes de relaciones, administrador de tablas de enrutamiento, tablas de enrutamiento, vistas](images/multrtabrel.png)

Una instancia del cliente se puede registrar varias veces con una instancia del administrador de tablas de enrutamiento, una vez por cada familia de direcciones. Un cliente se puede registrar con cada instancia del administrador de tablas de enrutamiento.

En la ilustración siguiente se muestra cómo se relacionan las entradas de la tabla de enrutamiento. Para obtener más información sobre las entradas de la tabla de enrutamiento, consulte entradas de la [tabla de enrutamiento](routing-table-entries.md).

![relación entre las entradas de la tabla de enrutamiento](images/nexthop.png)

La tabla de enrutamiento contiene destinos. Cada destino está relacionado con una o más rutas. Cada ruta tiene cero, uno o más punteros a los saltos siguientes que están asociados a la ruta. Cada puntero hace referencia al próximo salto real de la lista de próximos saltos. Cada cliente que se registra con el administrador de tablas de enrutamiento crea una lista de los saltos siguientes que el cliente posee.

Las rutas solo pueden contener punteros a la lista de próximo salto asociada al cliente que posee la ruta.

 

 




