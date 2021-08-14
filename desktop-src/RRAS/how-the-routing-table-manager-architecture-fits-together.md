---
title: Cómo encaja la arquitectura del administrador de tablas de enrutamiento
description: En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1637eed71a89a6de4fa7dad6a4fea4a5918366f69ee05a490824699605a117a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791379"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Cómo encaja la arquitectura del administrador de tablas de enrutamiento

En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.

![relación entre los componentes del enrutador](images/rtsrvarch.png)

Cuando se arranca el enrutador, se inicia el servicio de administrador de enrutadores, así como uno o varios protocolos de enrutamiento. Los protocolos de enrutamiento están asociados a las distintas interfaces del enrutador. El administrador de enrutadores también inicia el administrador de tablas de enrutamiento.

En la ilustración siguiente se muestra la relación entre los clientes y los distintos componentes del administrador de tablas de enrutamiento.

![relación entre clientes y componentes del administrador de tablas de enrutamiento](images/rtmentrel.png)

El administrador de enrutadores inicia una o varias instancias del administrador de tablas de enrutamiento. Cuando se inician varias instancias del administrador de tablas de enrutamiento, el enrutador se ha configurado para que actúe como uno o varios enrutadores virtuales. Cada instancia del administrador de tablas de enrutamiento posee una o varias interfaces; cada interfaz solo puede ser propiedad de una instancia del administrador de tablas de enrutamiento.

Cada instancia del administrador de tablas de enrutamiento es independiente de las demás. no se intercambia ninguna información entre las instancias de .

Cada instancia del administrador de tablas de enrutamiento contiene una o varias tablas de enrutamiento. Cada tabla de enrutamiento está asociada a una familia de direcciones.

Cada tabla de enrutamiento contiene una o varias vistas. En este ejemplo, la tabla de enrutamiento se muestra con una vista de unidifusión y multidifusión. Cada vista es un subconjunto de la tabla de enrutamiento.

En la ilustración siguiente se muestra la relación entre los clientes y varias instancias del administrador de tablas de enrutamiento, las tablas de enrutamiento y las vistas.

![clientes de relación, administrador de tablas de enrutamiento, tablas de enrutamiento, vistas](images/multrtabrel.png)

Una instancia del cliente puede registrarse varias veces con una instancia del administrador de tablas de enrutamiento, una vez por familia de direcciones. Un cliente puede registrarse con cada instancia del administrador de tablas de enrutamiento.

En la ilustración siguiente se muestra cómo se relacionan las entradas de la tabla de enrutamiento. Para obtener más información sobre las entradas de tabla de enrutamiento, vea [Entradas de tabla de enrutamiento](routing-table-entries.md).

![relación entre las entradas de tabla de enrutamiento](images/nexthop.png)

La tabla de enrutamiento contiene destinos. Cada destino está relacionado con una o varias rutas. Cada ruta tiene cero, uno o más punteros a los próximo saltos asociados a la ruta. Cada puntero hace referencia al próximo salto real en la lista de próximo saltos. Cada cliente que se registra con el administrador de tablas de enrutamiento crea una lista de próximo saltos que posee el cliente.

Las rutas solo pueden contener punteros a la lista de próximo salto asociada al cliente que posee la ruta.

 

 




