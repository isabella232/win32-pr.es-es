---
description: La inversión de prioridad se produce cuando dos o más subprocesos con prioridades diferentes están en contención para programarse.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversión de prioridades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a891655196b8f7e81c118d39fb8516a244411f1f4f6d9505e2fb40818d71f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031935"
---
# <a name="priority-inversion"></a>Inversión de prioridades

La inversión de prioridad se produce cuando dos o más subprocesos con prioridades diferentes están en contención para programarse. Considere un caso simple con tres subprocesos: subproceso 1, subproceso 2 y subproceso 3. El subproceso 1 es de alta prioridad y está listo para programarse. El subproceso 2, un subproceso de prioridad baja, está ejecutando código en una sección crítica. El subproceso 1, el subproceso de prioridad alta, comienza a esperar un recurso compartido del subproceso 2. El subproceso 3 tiene prioridad media. El subproceso 3 recibe todo el tiempo del procesador, porque el subproceso de prioridad alta (subproceso 1) está esperando recursos compartidos del subproceso de prioridad baja (subproceso 2). El subproceso 2 no abandonará la sección crítica, porque no tiene la prioridad más alta y no se programará.

El programador resuelve este problema al aumentar aleatoriamente la prioridad de los subprocesos listos (en este caso, los titulares de bloqueo de prioridad baja). Los subprocesos de prioridad baja se ejecutan lo suficiente como para salir de la sección crítica y el subproceso de prioridad alta puede entrar en la sección crítica. Si el subproceso de prioridad baja no obtiene suficiente tiempo de CPU para salir de la sección crítica la primera vez, tendrá otra oportunidad durante la siguiente ronda de programación.

 

 



