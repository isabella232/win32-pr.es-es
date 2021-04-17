---
description: El sistema operativo Windows acumula un conjunto de estadísticas de funcionamiento para estaciones de trabajo y servidores desde el momento en que se inicia el servicio de estación de trabajo o servidor.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funciones de estadísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678205"
---
# <a name="statistics-functions"></a>Funciones de estadísticas

El sistema operativo Windows acumula un conjunto de estadísticas de funcionamiento para estaciones de trabajo y servidores desde el momento en que se inicia el servicio de estación de trabajo o servidor. Para recuperar estas estadísticas, puede llamar a la siguiente función de estadísticas de administración de redes.



| Función                                     | Descripción                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Recupera las estadísticas de funcionamiento de un servicio. admite los servicios de estación de trabajo y servidor. |



 

La función **NetStatisticsGet** devuelve una estructura de la [**estación de trabajo de STAT \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) cuando se solicitan estadísticas de la estación de trabajo; la función devuelve una estructura de [**\_ servidor \_**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) de estadísticas cuando se solicitan estadísticas del servidor.

 

 



