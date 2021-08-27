---
title: Marcas de ruta
description: Marcas de ruta
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Ruta
- Marcas de ruta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1476742f1204eb14dd2bb96b289825d179a58e5bec01ff0aee18bcfbdb13a9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081245"
---
# <a name="route-flags"></a>Marcas de ruta

## <a name="state-of-the-route-constants"></a>Estado de las constantes de ruta



| Constante                    | Value | Descripción             |
|-----------------------------|-------|-------------------------|
| ESTADO DE \_ RUTA RTM \_ \_ CREADO  | 0     | Se ha creado la ruta. |
| ELIMINACIÓN DEL \_ ESTADO DE LA RUTA \_ \_ RTM | 1     | La ruta se está eliminando. |
| ESTADO DE \_ RUTA RTM \_ \_ ELIMINADO  | 2     | Se ha eliminado la ruta. |



 

## <a name="route-update-flags"></a>Marcas de actualización de rutas



| Constante                  | Value      | Descripción                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAMBIO DE RUTA DE RTM \_ \_ \_ PRIMERO | 0x01       | Indica que el administrador de tablas de enrutamiento no debe comprobar el miembro **De la estructura** [**\_ RTM ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) al determinar cuándo dos rutas son iguales. |
| CAMBIO DE \_ RUTA RTM \_ \_ NUEVO   | 0x02       | Devuelto por el administrador de tablas de enrutamiento para indicar que se creó una nueva ruta.                                                                                                                 |
| MEJOR CAMBIO \_ DE RUTA \_ DE RTM \_  | 0x00010000 | Devuelto por el administrador de tablas de enrutamiento para indicar que la ruta que se agregó o actualizó era la mejor, o que debido al cambio, una nueva ruta se convirtió en la mejor ruta.           |



 

## <a name="unicast-flags"></a>Marcas de unidifusión



| Constante                  | Value  | Descripción                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| MARCAS DE RUTA DE RTM \_ \_ \_ LOCALES  | 0x0010 | Indica que un destino está en una red accesible directamente.            |
| MARCAS DE \_ RUTA \_ RTM \_ REMOTAS | 0x0020 | Indica que el destino no está en una red accesible directamente. |
| RTM \_ ROUTE \_ FLAGS \_ MYSELF | 0x0040 | Indica que el destino es una de las direcciones del enrutador.            |



 

## <a name="broadcast-and-multicast-flags"></a>Marcas de difusión y multidifusión



| Constante                           | Value  | Descripción                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCAST \_ DE MARCAS DE RUTA \_ DE RTM \_           | 0x0100 | Indica que esta ruta es una ruta a una dirección de multidifusión.                                                                                                                                               |
| MCAST \_ LOCAL DE MARCAS DE \_ \_ RUTA DE \_ RTM    | 0x0200 | Indica que esta ruta es una ruta a una dirección de multidifusión local.                                                                                                                                         |
| MARCAS DE \_ \_ RUTAS RTM \_ LIMITADAS \_ BC     | 0x0400 | Indica que esta ruta es una dirección de difusión limitada. No se deben reenviar los paquetes a este destino.                                                                                             |
| RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ NETBC    | 0x1000 | Indica que el destino coincide con la dirección de difusión de todos los ceros de una interfaz. Si el reenvío de difusión está habilitado, los paquetes deben recibirse y reenviarse a todas las interfaces adecuadas.               |
| RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC | 0x2000 | Indica que el destino coincide con la dirección de difusión de subred de todos los ceros de una interfaz. Si el reenvío de difusión de subred está habilitado, se deben recibir paquetes y reenviar todas las interfaces adecuadas. |
| MARCAS DE RUTA DE RTM \_ \_ \_ \_ NETBC     | 0x4000 | Indica que el destino coincide con la dirección de difusión de todos los usuarios de una interfaz. Si el reenvío de difusión está habilitado, los paquetes deben recibirse y reenviarse a todas las interfaces adecuadas.                |
| RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNETBC  | 0x8000 | Indica que el destino coincide con la dirección de difusión de subred de todos los usuarios de una interfaz. Si el reenvío de difusión de subred está habilitado, se deben recibir paquetes y reenviar todas las interfaces adecuadas.  |



 

## <a name="grouping-of-flags"></a>Agrupación de marcas



| Grupo                            | Miembros                                                                                                                                                                  | Descripción                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| REENVÍO DE \_ MARCAS \_ DE RUTA DE RTM \_    | MARCAS DE \_ \_ RUTAS RTM MARFRACCIÓN, MARCAS DE RUTA \_ \_ \_ RTM \_ BLACKHOLE, RTM \_ ROUTE \_ FLAGS \_ DISCARD, RTM \_ ROUTE \_ FLAGS \_ INACTIVE                                                        | Especifica las marcas de reenvío.                          |
| RTM \_ ROUTE MARCA CUALQUIER \_ \_ \_ UNIDIFUSIÓN  | MARCAS DE RUTA DE RTM LOCALES, MARCAS DE \_ \_ RUTA DE \_ RTM \_ \_ \_ REMOTAS, MARCAS DE RUTA \_ \_ RTM \_ YO MISMO                                                                                           | Especifica las marcas de unidifusión.                             |
| RTM \_ ROUTE MARCA CUALQUIER \_ \_ \_ MCAST    | MCAST \_ DE MARCAS DE RUTA DE \_ \_ RTM, MCAST \_ DE MARCAS DE RUTA \_ DE \_ \_ RTM                                                                                                                | Especifica las marcas de unidifusión.                             |
| RTM \_ ROUTE \_ FLAGS \_ SUBNET \_ BCAST | RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNET \_ BC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC                                                                                                  | Especifica las marcas de difusión de subred.                    |
| RTM \_ ROUTE \_ FLAGS \_ NET \_ BCAST    | MARCAS DE RUTA DE RTM \_ \_ \_ \_ NETBC, MARCAS \_ DE RUTA \_ RTM \_ CEROS \_ NETBC                                                                                                          | Especifica las marcas de difusión de toda la red.                  |
| RTM \_ ROUTE MARCA CUALQUIER \_ \_ \_ BCAST    | RTM \_ ROUTE \_ FLAGS \_ LIMITED \_ BC, RTM \_ ROUTE \_ FLAGS \_ ONES \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNET \_ BC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC | Especifica cualquiera de las marcas de difusión de toda la red o subred. |



 

 

 




