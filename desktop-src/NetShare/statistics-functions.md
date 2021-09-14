---
description: El Windows operativo acumula un conjunto de estadísticas de funcionamiento para estaciones de trabajo y servidores desde el momento en que se inicia la estación de trabajo o el servicio de servidor.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funciones de estadísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245090"
---
# <a name="statistics-functions"></a>Funciones de estadísticas

El Windows operativo acumula un conjunto de estadísticas de funcionamiento para estaciones de trabajo y servidores desde el momento en que se inicia la estación de trabajo o el servicio de servidor. Para recuperar estas estadísticas, puede llamar a la siguiente función de estadísticas de administración de red.



| Función                                     | Descripción                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Recupera las estadísticas operativas de un servicio; admite los servicios de estación de trabajo y servidor. |



 

La **función NetStatisticsGet** devuelve una estructura [**STAT WORKSTATION \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) cuando se solicitan estadísticas de estación de trabajo; la función devuelve una estructura [**STAT SERVER \_ \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) cuando se solicitan estadísticas de servidor.

 

 



