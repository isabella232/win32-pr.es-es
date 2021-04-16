---
description: Funciones de depuración de sección crítica
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funciones de depuración de sección crítica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536897"
---
# <a name="critical-section-debugging-functions"></a>Funciones de depuración de sección crítica

Estas funciones ayudan a depurar las secciones críticas en el código, lo que puede facilitar la búsqueda de la causa de un interbloqueo. Estas funciones usan la clase auxiliar [**CCritSec**](ccritsec.md) .



| Función                             | Descripción                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Devuelve **true** si el subproceso actual posee la sección crítica especificada.  |
| [**CritCheckOut**](critcheckout.md) | Devuelve **false** si el subproceso actual posee la sección crítica especificada. |
| [**DbgLockTrace**](dbglocktrace.md) | Habilita o deshabilita el registro de depuración de una sección crítica determinada.              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de depuración](debugging-utilities.md)
</dt> </dl>

 

 



