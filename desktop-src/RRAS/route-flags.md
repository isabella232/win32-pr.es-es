---
title: Marcas de ruta
description: Marcas de ruta
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Ruta
- Marcas de ruta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1711ef4ed621d55cc00302cca181676a3892c030
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993959"
---
# <a name="route-flags"></a>Marcas de ruta

## <a name="state-of-the-route-constants"></a>Estado de las constantes de ruta



| Constante                    | Value | Descripción             |
|-----------------------------|-------|-------------------------|
| \_Estado de ruta RTM \_ \_ creado  | 0     | Se ha creado la ruta. |
| eliminación del estado de la \_ ruta RTM \_ \_ | 1     | La ruta se está eliminando. |
| \_Estado de ruta RTM \_ \_ eliminado  | 2     | La ruta se ha eliminado. |



 

## <a name="route-update-flags"></a>Marcas de actualización de ruta



| Constante                  | Value      | Descripción                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_cambio de ruta RTM \_ \_ primero | 0x01       | Indica que el administrador de tabla de enrutamiento no debe comprobar el miembro de **vecino** de la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) al determinar si dos rutas son iguales. |
| cambio de ruta de RTM \_ \_ \_ nuevo   | 0x02       | Lo devuelve el administrador de tablas de enrutamiento para indicar que se ha creado una nueva ruta.                                                                                                                 |
| cambio de ruta de RTM \_ \_ \_ mejor  | 0x00010000 | Lo devuelve el administrador de tablas de enrutamiento para indicar que la ruta que se agregó o actualizó era la mejor ruta, o que debido al cambio, una nueva ruta se convirtió en la mejor ruta.           |



 

## <a name="unicast-flags"></a>Marcas de unidifusión



| Constante                  | Value  | Descripción                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| \_marcas de ruta RTM \_ \_ local  | 0x0010 | Indica que un destino está en una red directamente accesible.            |
| \_marcas de ruta RTM \_ \_ remotas | 0x0020 | Indica que el destino no se encuentra en una red directamente accesible. |
| \_marcas de ruta RTM \_ \_ | 0x0040 | Indica que el destino es una de las direcciones del enrutador.            |



 

## <a name="broadcast-and-multicast-flags"></a>Marcas de difusión y multidifusión



| Constante                           | Value  | Descripción                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_marcas de ruta RTM \_ \_ MCAST           | 0x0100 | Indica que esta ruta es una ruta a una dirección de multidifusión.                                                                                                                                               |
| \_marcas de ruta RTM \_ \_ \_ MCAST locales    | 0x0200 | Indica que esta ruta es una ruta a una dirección de multidifusión local.                                                                                                                                         |
| las \_ marcas de ruta RTM de \_ \_ \_ BC limitado     | 0x0400 | Indica que esta ruta es una dirección de difusión limitada. No se deben reenviar los paquetes a este destino.                                                                                             |
| \_marcas de ruta RTM \_ \_ ceros \_ NETBC    | 0x1000 | Indica que el destino coincide con la dirección de difusión de todos los ceros de una interfaz. Si está habilitado el reenvío de difusión, los paquetes se deben recibir y reenviar todas las interfaces adecuadas.               |
| \_marcas de ruta RTM \_ \_ ceros \_ SUBNETBC | 0x2000 | Indica que el destino coincide con la dirección de difusión de subred de todos los ceros de una interfaz. Si está habilitado el reenvío de difusión de subred, los paquetes se deben recibir y reenviar todas las interfaces adecuadas. |
| \_marcas de ruta RTM \_ \_ \_ NETBC     | 0x4000 | Indica que el destino coincide con la dirección de difusión de todas las interfaces de una interfaz. Si está habilitado el reenvío de difusión, los paquetes se deben recibir y reenviar todas las interfaces adecuadas.                |
| \_marcas de ruta RTM \_ \_ \_ SUBNETBC  | 0x8000 | Indica que el destino coincide con una dirección de difusión de subred de todas las interfaces de una interfaz. Si está habilitado el reenvío de difusión de subred, los paquetes se deben recibir y reenviar todas las interfaces adecuadas.  |



 

## <a name="grouping-of-flags"></a>Agrupación de marcas



| Grupo                            | Miembros                                                                                                                                                                  | Descripción                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| reenvío de \_ marcas de ruta RTM \_ \_    | \_marcas de ruta RTM \_ \_ Martian, marcas de \_ ruta RTM \_ \_ negras, \_ marcas de ruta RTM \_ \_ DEScartadas, marcas de ruta RTM \_ \_ \_ inactivas                                                        | Especifica cualquier marcador de reenvío.                          |
| la \_ ruta de RTM \_ marca \_ cualquier \_ unidifusión  | \_ \_ marcas de ruta RTM locales, las marcas \_ de \_ ruta RTM \_ \_ remotos y las \_ marcas de ruta RTM \_ \_                                                                                           | Especifica las marcas de unidifusión.                             |
| la \_ ruta RTM \_ marca \_ cualquier \_ MCAST    | \_ \_ marcas de ruta RTM \_ MCAST, \_ marcas de ruta RTM \_ \_ \_ MCAST locales                                                                                                                | Especifica las marcas de unidifusión.                             |
| BCAST de la subred de marcas de \_ ruta RTM \_ \_ \_ | la \_ ruta RTM \_ marca una \_ \_ subred \_ BC, \_ marcas de ruta RTM \_ \_ ceros \_ SUBNETBC                                                                                                  | Especifica las marcas de difusión de subred.                    |
| \_marcas de ruta RTM \_ \_ net \_ BCAST    | las \_ \_ marcas de ruta RTM \_ \_ NETBC, \_ marcas de ruta RTM \_ \_ ceros \_ NETBC                                                                                                          | Especifica las marcas de difusión de red.                  |
| la \_ ruta RTM \_ marca \_ cualquier \_ BCAST    | la \_ ruta RTM \_ marca el \_ \_ BC limitado, las marcas de ruta RTM \_ \_ \_ \_ NETBC, las marcas de ruta RTM de la \_ \_ \_ \_ subred \_ BC, \_ marcas de ruta RTM \_ \_ ceros \_ NETBC, \_ marcas de ruta RTM \_ \_ ceros \_ SUBNETBC | Especifica cualquiera de las marcas de difusión de subred o de red. |



 

 

 




