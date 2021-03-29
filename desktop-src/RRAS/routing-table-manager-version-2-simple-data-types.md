---
title: Tipos de datos simples del administrador de tablas de enrutamiento versión 2
description: La API RTMv2 define varios tipos de datos simples. En la tabla siguiente se enumeran estos tipos de datos.
ms.assetid: e935518e-b8d8-47fb-b2b2-c9750c2b540e
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 2, tipos de datos simples
- Administrador de tablas de enrutamiento versión 2 RRAS, tipos de datos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dbd7530799c1c7e1702e0384d51b37a77dda0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777623"
---
# <a name="routing-table-manager-version-2-simple-data-types"></a>Tipos de datos simples del administrador de tablas de enrutamiento versión 2

La API RTMv2 define varios tipos de datos simples. En la tabla siguiente se enumeran estos tipos de datos.



| Tipo de datos                                                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                      | Definición de tipo              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| \_ \_ ID. de vista de RTM, \* \_ ID. de vista de PRTM \_                                                                                                                                                                                                                                                                                             | Identifica una vista determinada.                                                                                                                    | INT                  |
| \_ \_ conjunto de vistas de DWORD RTM, \* \_ conjunto de vistas PRTM \_                                                                                                                                                                                                                                                                                     | Identifica un conjunto de vistas; se expresa como una máscara.                                                                                                  | DWORD                |
| \_ \_ identificador de entidad de RTM, \* identificador de entidad de PRTM \_ \_ , identificador de \_ destino de RTM \_ , \* \_ identificador de destino de PRTM, identificador de \_ \_ ruta de RTM, identificador de ruta de PRTM, identificador de salto de RTM \_ , \* \_ \_ \_ \_ \* \_ \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ \_ identificador de tipo de salto de versión de RTM, identificador de enumeración de la lista de distribución, PRTM | Controla la señalización de datos de RTMv2.                                                                                                                  | HANDLE               |
| \_ \_ \_ tipo de método de entidad RTM, \* \_ tipo de método PRTM Entity \_ \_                                                                                                                                                                                                                                                                     | Identifica los métodos exportados por un cliente registrado.                                                                                              | DWORD                |
| \_ \_ método de exportación de la entidad RTM \_ , \* \_ método de exportación de entidad PRTM \_ \_                                                                                                                                                                                                                                                                 | Especifica el prototipo común para los métodos de cliente.                                                                                               | \_ENTITY ( \_ método)     |
| \_ \_ \_ marcas de cambio de ruta RTM, \* marcas de \_ cambio de ruta PRTM \_ \_                                                                                                                                                                                                                                                                     | Marcas de entrada y salida que se usan para especificar el estado cuando se agrega o actualiza una ruta.                                                               | DWORD                |
| las \_ \_ \_ marcas de cambio de NextHop de RTM, \* marcas de cambio de PRTM \_ NextHop \_ \_                                                                                                                                                                                                                                                                 | Marcas de salida que se usan para especificar el estado cuando se agrega un próximo salto.                                                                                 | DWORD                |
| \_ \_ marcas de coincidencia de RTM, \* marcas de coincidencia de PRTM \_ \_                                                                                                                                                                                                                                                                                     | Marcas de entrada que se usan para especificar criterios al buscar coincidencias en las rutas de la tabla de enrutamiento.                                                                  | DWORD                |
| \_marcas de enumeración RTM \_ , \* marcas de \_ enumeración PRTM \_                                                                                                                                                                                                                                                                                       | Identifica las enumeraciones.                                                                                                                         | DWORD                |
| \_ \_ marcas de notificación de RTM, \* marcas de notificación de PRTM \_ \_                                                                                                                                                                                                                                                                                   | Marcas de salida utilizadas para especificar el tipo de notificación que se va a emitir; se compone de la siguiente manera: (cambiar tipos \| de destino) en el que está interesado un cliente. | DWORD                |
| \_ \_ devolución de llamada de evento RTM, \* devolución de llamada de \_ evento PRTM \_ ;                                                                                                                                                                                                                                                                              | Identifica la devolución de llamada que se usa para notificar a los clientes que se ha producido un cambio en el estado de la ruta o en los clientes registrados.                                  | devolución de llamada de \_ evento RTM \_ |



 

 

 




