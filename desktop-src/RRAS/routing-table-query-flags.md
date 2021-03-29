---
title: Marcas de consulta de tabla de enrutamiento
description: Use estas constantes para las consultas de tabla de enrutador.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Marcas de consulta de tabla de enrutamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903915"
---
# <a name="routing-table-query-flags"></a>Marcas de consulta de tabla de enrutamiento

Use estas constantes para las consultas de tabla de enrutador.



| Constante              | Value      | Descripción                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| RTM no \_ coincide con \_ ninguno      | 0x00000000 | Coincide con ninguno de los criterios; se devuelven todas las rutas para el destino. |
| propietario de la coincidencia de RTM \_ \_     | 0x00000001 | Coincide con las rutas con el mismo propietario.                                            |
| \_vecino de coincidencia de RTM \_ | 0x00000002 | Coincide con las rutas con el mismo vecino.                                     |
| \_preferencias de coincidencia de RTM \_      | 0x00000004 | Coincide con las rutas que tienen la misma preferencia.                              |
| \_próximo salto de coincidencia de RTM \_   | 0x00000008 | Coincide con las rutas que tienen el mismo salto siguiente.                                |
| \_interfaz de coincidencia de RTM \_ | 0x00000010 | Coincide con las rutas que se encuentran en la misma interfaz.                             |
| \_coincidencia \_ completa de RTM      | 0x0000FFFF | Coincide con rutas con todos los criterios.                                          |
| \_mejor \_ Protocolo RTM   | 0          | Devuelve una ruta sin tener en consideración el protocolo que la posea.                      |
| RTM \_ este \_ Protocolo   | ~0         | Devuelve la mejor ruta para el protocolo de llamada.                           |



 

 

 




