---
title: Contadores, consultas y predicación
description: Los contadores de salida de flujo y UAV funcionan en Direct3D 12 en un método similar a Direct3D 11, aunque ahora la aplicación debe asignar memoria para los contadores, el controlador no lo hace.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466366"
---
# <a name="counters-queries-and-predication"></a>Contadores, consultas y predicación

En este tema se tratan los contadores de salida de flujo, los contadores UAV, las consultas y el predicado.

Los contadores de salida de flujo y UAV funcionan en Direct3D 12 en un método similar a Direct3D 11, aunque ahora la aplicación debe asignar memoria para los contadores, el controlador no lo hace. Las consultas de Direct3D 12 son más diferentes de las de Direct3D 11, con la adición de barreras y otros procesos que eliminan la necesidad de algunos tipos de consulta.

## <a name="in-this-section"></a>En esta sección



| Tema                                                           | Descripción                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contadores de salida de flujo](stream-output-counters.md)<br/> | La salida de secuencia es la capacidad de la GPU de escribir vértices en un búfer. Los contadores de salida de flujo supervisan el progreso.<br/>                                                               |
| [Contadores de UAV](uav-counters.md)<br/>                     | Los contadores UAV se pueden usar para asociar un contador atómico de 32 bits a una vista de acceso desordenada (UAV).<br/>                                                                                |
| [Consultas](queries.md)<br/>                               | En Direct3D 12, las consultas se agrupan en matrices de consultas denominadas montón de consultas. Un montón de consultas tiene un tipo que define los tipos válidos de consultas que se pueden usar con ese montón.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Medición del rendimiento](performance-measurement.md)
</dt> </dl>

 

 





