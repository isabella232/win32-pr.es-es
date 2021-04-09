---
description: Los expertos que exportan la función ejecutar o configurar solo pueden llamar a las siguientes funciones auxiliares.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funciones de experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907679"
---
# <a name="expert-functions"></a>Funciones de experto

Los expertos que exportan la función [Ejecutar](run.md) o [configurar](configure.md) solo pueden llamar a las siguientes funciones auxiliares.



| Función                                         | Descripción                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ExpertGetFrame](expertgetframe.md)             | Recupera un fotograma determinado de la captura.                                               |
| [ExpertIndicateStatus](expertindicatestatus.md) | Indica el porcentaje de finalización del análisis de captura del experto.             |
| [ExpertGetStartupInfo](expertgetstartupinfo.md) | Recupera la información de inicio del experto.                                       |
| [ExpertMemorySize](expertmemorysize.md)         | Recupera el tamaño de la memoria asignada por una llamada a la función **ExpertAllocMemory** . |
| [ExpertSubmitEvent](expertsubmitevent.md)       | Indica un problema y recupera información sobre el problema si existe uno.          |
| [ExpertAllocMemory](expertallocmemory.md)       | Asigna memoria para el experto.                                                        |
| [ExpertReallocMemory](expertreallocmemory.md)   | Cambia el tamaño de la memoria asignada por la función **ExpertAllocMemory** .         |
| [ExpertFreeMemory](expertfreememory.md)         | Libera la memoria asignada por el experto.                                                   |



 

Para obtener información sobre las funciones de exportación, las funciones auxiliares a las que pueden llamar expertos y analizadores, estructuras y enumeraciones, vea los temas siguientes:



| Para información acerca de                                             | Vea                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones exportadas por expertos                            | [Funciones de exportación de archivos DLL de experto](expert-dll-export-functions.md)               |
| Estructuras usadas por las funciones de expertos                      | [Estructuras expertas](expert-structures.md)                                   |
| Enumeraciones usadas por las estructuras y funciones de expertos              | [Enumeraciones de experto](expert-enumerations.md)                               |
| Funciones auxiliares comunes a las que pueden llamar expertos y analizadores | [Funciones comunes de experto y analizador](expert-and-parser-common-functions.md) |



 

 

 



