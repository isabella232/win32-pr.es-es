---
title: Marcas de consulta de tabla de enrutamiento
description: Use estas constantes para las consultas de tabla de enrutador.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Marcas de consulta de tabla de enrutamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 307dd91e9b3d248e5b2b69869ee1e7d14ae17834f7fe57d9e136da16ba3f6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787453"
---
# <a name="routing-table-query-flags"></a>Marcas de consulta de tabla de enrutamiento

Use estas constantes para las consultas de tabla de enrutador.



| Constante              | Valor      | Descripción                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| RTM \_ MATCH \_ NONE      | 0x00000000 | No coincide con ninguno de los criterios; se devuelven todas las rutas del destino. |
| PROPIETARIO DE COINCIDENCIA DE RTM \_ \_     | 0x00000001 | Coincide con las rutas con el mismo propietario.                                            |
| RTM \_ MATCH \_ LOT MES | 0x00000002 | Coincide con las rutas con el mismo vecino.                                     |
| RTM \_ MATCH \_ PREF      | 0x00000004 | Coincide con las rutas que tienen la misma preferencia.                              |
| RTM \_ MATCH \_ NEXTHOP   | 0x00000008 | Coincide con las rutas que tienen el mismo próximo salto.                                |
| INTERFAZ DE COINCIDENCIA DE RTM \_ \_ | 0x00000010 | Coincide con las rutas que están en la misma interfaz.                             |
| RTM \_ MATCH \_ FULL      | 0x0000FFFF | Coincide con las rutas con todos los criterios.                                          |
| MEJOR \_ PROTOCOLO RTM \_   | 0          | Devuelve una ruta independientemente del protocolo que la posee.                      |
| RTM \_ ESTE \_ PROTOCOLO   | ~0         | Devuelve la mejor ruta para el protocolo de llamada.                           |



 

 

 




