---
description: La inversión de prioridad se produce cuando dos o más subprocesos con prioridades diferentes están en la contención que se va a programar.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversión de prioridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360690"
---
# <a name="priority-inversion"></a>Inversión de prioridad

La inversión de prioridad se produce cuando dos o más subprocesos con prioridades diferentes están en la contención que se va a programar. Considere un caso sencillo con tres subprocesos: el subproceso 1, el subproceso 2 y el subproceso 3. El subproceso 1 tiene prioridad alta y está listo para ser programado. Thread 2, un subproceso de prioridad baja, ejecuta código en una sección crítica. El subproceso 1, el subproceso de prioridad alta, comienza a esperar a un recurso compartido del subproceso 2. El subproceso 3 tiene prioridad media. El subproceso 3 recibe todo el tiempo de procesador, porque el subproceso de prioridad alta (subproceso 1) está esperando los recursos compartidos del subproceso de prioridad baja (subproceso 2). El subproceso 2 no abandonará la sección crítica porque no tiene la prioridad más alta y no se programará.

El programador resuelve este problema al aumentar aleatoriamente la prioridad de los subprocesos listos (en este caso, los bloqueadores de baja prioridad). Los subprocesos de prioridad baja se ejecutan el tiempo suficiente para salir de la sección crítica y el subproceso de prioridad alta puede entrar en la sección crítica. Si el subproceso de prioridad baja no obtiene suficiente tiempo de CPU para salir de la sección crítica la primera vez, obtendrá otra oportunidad durante la siguiente ronda de programación.

 

 



