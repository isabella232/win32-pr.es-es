---
description: Funciones de depuración de sección crítica
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funciones de depuración de sección crítica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160179"
---
# <a name="critical-section-debugging-functions"></a>Funciones de depuración de sección crítica

Estas funciones ayudan a depurar secciones críticas en el código, lo que puede facilitar la búsqueda de la causa de un interbloqueo. Estas funciones usan la [**clase auxiliar CCritSec.**](ccritsec.md)



| Función                             | Descripción                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Devuelve **TRUE** si el subproceso actual posee la sección crítica especificada.  |
| [**CritCheckOut**](critcheckout.md) | Devuelve **FALSE** si el subproceso actual posee la sección crítica especificada. |
| [**DbgLockTrace**](dbglocktrace.md) | Habilita o deshabilita el registro de depuración para una sección crítica determinada.              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilidades de depuración](debugging-utilities.md)
</dt> </dl>

 

 



