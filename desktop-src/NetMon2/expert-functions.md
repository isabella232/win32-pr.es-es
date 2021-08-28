---
description: Los expertos que exportan la función Ejecutar o configurar solo pueden llamar a las siguientes funciones auxiliares.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funciones expertos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b189f0af3b748bc6ad162342ae23d98cbf0e381232193c114d245fa6aadb77c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779385"
---
# <a name="expert-functions"></a>Funciones expertos

Los expertos que exportan la función [Ejecutar](run.md) o configurar solo pueden llamar a las [siguientes funciones auxiliares.](configure.md)



| Función                                         | Descripción                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ExpertGetFrame](expertgetframe.md)             | Recupera un fotograma determinado de la captura.                                               |
| [ExpertIndicateStatus](expertindicatestatus.md) | Indica el porcentaje de finalización del análisis de captura del experto.             |
| [ExpertGetStartupInfo](expertgetstartupinfo.md) | Recupera la información de inicio del experto.                                       |
| [ExpertMemorySize](expertmemorysize.md)         | Recupera el tamaño de memoria asignado por una llamada a la **función ExpertAllocMemory.** |
| [ExpertSubmitEvent](expertsubmitevent.md)       | Indica un problema y recupera información sobre el problema si existe.          |
| [ExpertAllocMemory](expertallocmemory.md)       | Asigna memoria para el experto.                                                        |
| [ExpertReallocMemory](expertreallocmemory.md)   | Cambia el tamaño de la memoria asignada por la **función ExpertAllocMemory.**         |
| [ExpertFreeMemory](expertfreememory.md)         | Libera la memoria asignada por el experto.                                                   |



 

Para obtener información sobre las funciones de exportación, las funciones auxiliares a las que pueden llamar expertos y analizadores, estructuras y enumeraciones, vea los temas siguientes:



| Para información acerca de                                             | Vea                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones exportadas por expertos                            | [Funciones de exportación de DLL expertos](expert-dll-export-functions.md)               |
| Estructuras utilizadas por funciones expertos                      | [Estructuras expertos](expert-structures.md)                                   |
| Enumeraciones usadas por funciones y estructuras expertos              | [Enumeraciones de expertos](expert-enumerations.md)                               |
| Funciones auxiliares comunes a las que pueden llamar expertos y analizadores | [Funciones comunes de expertos y analizadores](expert-and-parser-common-functions.md) |



 

 

 



