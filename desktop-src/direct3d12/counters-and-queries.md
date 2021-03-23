---
title: Contadores, consultas y predication
description: Los contadores de salida de flujo y UAV funcionan en Direct3D 12 en un método similar a Direct3D 11, aunque ahora la aplicación debe asignar la memoria para los contadores, el controlador no lo hace.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104549170"
---
# <a name="counters-queries-and-predication"></a>Contadores, consultas y predication

En este tema se describen los contadores de salida de flujo, los contadores de UAV, las consultas y predication.

Los contadores de salida de flujo y UAV funcionan en Direct3D 12 en un método similar a Direct3D 11, aunque ahora la aplicación debe asignar la memoria para los contadores, el controlador no lo hace. Las consultas en Direct3D 12 son más diferentes de las de Direct3D 11, con la adición de barreras y otros procesos que eliminan la necesidad de algunos tipos de consulta.

## <a name="in-this-section"></a>En esta sección



| Tema                                                           | Descripción                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contadores de salida de flujo](stream-output-counters.md)<br/> | La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer. Los contadores de salida de flujo supervisan el progreso.<br/>                                                               |
| [Contadores de UAV](uav-counters.md)<br/>                     | Los contadores de UAV se pueden usar para asociar un contador atómico de 32 bits con un desordenado-Access-View (UAV).<br/>                                                                                |
| [Consultas](queries.md)<br/>                               | En Direct3D 12, las consultas se agrupan en matrices de consultas llamadas un montón de consultas. Un montón de consulta tiene un tipo que define los tipos válidos de consultas que se pueden usar con ese montón.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Medición del rendimiento](performance-measurement.md)
</dt> </dl>

 

 





