---
title: Tipos de datos simples de Routing Table Manager versión 2
description: La API RTMv2 define varios tipos de datos simples. En la tabla siguiente se enumeran estos tipos de datos.
ms.assetid: e935518e-b8d8-47fb-b2b2-c9750c2b540e
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, Routing Table Manager versión 2, tipos de datos simples
- RRAS de la versión 2 de Routing Table Manager, tipos de datos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ae258f085915ed36355148e5a200989be0cab4703ea5bf6cebeda850af8f00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035995"
---
# <a name="routing-table-manager-version-2-simple-data-types"></a>Tipos de datos simples de Routing Table Manager versión 2

La API RTMv2 define varios tipos de datos simples. En la tabla siguiente se enumeran estos tipos de datos.



| Tipo de datos                                                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                      | Definición de tipo              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| ID. \_ DE VISTA DE RTM, \_ \* \_ ID. DE VISTA DE PRTM \_                                                                                                                                                                                                                                                                                             | Identifica una vista determinada.                                                                                                                    | INT                  |
| CONJUNTO DE VISTAS DE DWORD \_ \_ RTM, CONJUNTO DE \* VISTAS PRTM \_ \_                                                                                                                                                                                                                                                                                     | Identifica un conjunto de vistas; expresado como una máscara.                                                                                                  | DWORD                |
| IDENTIFICADOR DE ENTIDAD RTM, IDENTIFICADOR DE ENTIDAD PRTM, IDENTIFICADOR DEST DE RTM, IDENTIFICADOR DE DEST DE PRTM, IDENTIFICADOR DE RUTA RTM, IDENTIFICADOR DE RUTA DE \_ \_ \* \_ PRTM, IDENTIFICADOR NEXTHOP DE \_ PRTM, IDENTIFICADOR \_ \_ \* \_ \_ \_ \_ \* \_ \_ \_ \_ \* \_ \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ DE ENUMERACIÓN \_ RTM, IDENTIFICADOR DE ENUMERACIÓN DE PRTM, IDENTIFICADOR DE LISTA DE RUTAS RTM, IDENTIFICADOR DE LISTA DE RUTAS DE PRTM, IDENTIFICADOR DE NOTIFICACIÓN DE RTM, IDENTIFICADOR DE NOTIFICACIÓN DE PRTM | Controla los datos que apuntan a RTMv2.                                                                                                                  | HANDLE               |
| TIPO DE MÉTODO \_ DE \_ ENTIDAD \_ RTM, \* TIPO DE MÉTODO DE \_ \_ ENTIDAD PRTM \_                                                                                                                                                                                                                                                                     | Identifica los métodos exportados por un cliente registrado.                                                                                              | DWORD                |
| MÉTODO DE \_ EXPORTACIÓN \_ DE ENTIDADES \_ RTM, \* MÉTODO DE EXPORTACIÓN DE ENTIDADES PRTM \_ \_ \_                                                                                                                                                                                                                                                                 | Especifica el prototipo común para los métodos de cliente.                                                                                               | \_ENTITY \_ METHOD     |
| MARCAS DE CAMBIO \_ DE RUTA DE RTM, MARCAS DE CAMBIO DE \_ \_ RUTA \* PRTM \_ \_ \_                                                                                                                                                                                                                                                                     | Marcas de entrada y salida usadas para especificar el estado cuando se agrega o actualiza una ruta.                                                               | DWORD                |
| MARCAS DE \_ CAMBIO NEXTHOP DE \_ RTM, MARCAS DE CAMBIO \_ \* \_ NEXTHOP DE PRTM \_ \_                                                                                                                                                                                                                                                                 | Marcas de salida usadas para especificar el estado cuando se agrega un próximo salto.                                                                                 | DWORD                |
| MARCAS DE \_ COINCIDENCIA DE RTM, MARCAS DE \_ COINCIDENCIA DE \* PRTM \_ \_                                                                                                                                                                                                                                                                                     | Marcas de entrada usadas para especificar criterios al coincidir con rutas en la tabla de enrutamiento.                                                                  | DWORD                |
| MARCAS \_ DE \_ ENUMERACIÓN RTM, \* MARCAS \_ DE ENUMERACIÓN PRTM \_                                                                                                                                                                                                                                                                                       | Identifica enumeraciones.                                                                                                                         | DWORD                |
| MARCAS DE \_ NOTIFICACIÓN DE RTM, MARCAS DE \_ NOTIFICACIÓN DE \* PRTM \_ \_                                                                                                                                                                                                                                                                                   | Marcas de salida que se usan para especificar qué tipo de notificación se emite; compuesto de la siguiente manera: (Cambios de tipos \| dests) en el que está interesado un cliente. | DWORD                |
| RTM \_ EVENT \_ CALLBACK, \* PRTM \_ EVENT \_ CALLBACK;                                                                                                                                                                                                                                                                              | Identifica la devolución de llamada utilizada para notificar a los clientes que se ha producido un cambio en el estado de la ruta o en los clientes registrados.                                  | DEVOLUCIÓN DE LLAMADA \_ DE EVENTOS RTM \_ |



 

 

 




