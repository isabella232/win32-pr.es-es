---
description: Grupo de métodos que se usa para manipular bloqueos.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Métodos CShareLockLOCK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97234d65a3be75ffc1eb679db31360aa6ce6c416d879c67c0ffc5385e10bdb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654655"
---
# <a name="csharelocknh-methods"></a>Métodos CShareLockLOCK

Grupo de métodos que se usa para manipular bloqueos.

## <a name="methods"></a>Métodos

Estos son los métodos exportados por Rwnh.dll.



| Método                                                                   | Descripción                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**ExclusiveLock**](csharelocknh--exclusivelock.md)                     | Adquiere un bloqueo de lector/escritor.                                  |
| [**ExclusiveToPartial**](csharelocknh--exclusivetopartial.md)           | Cambia el estado.                                              |
| [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)                 | Libera un bloqueo.                                                |
| [**FirstPartialToExclusive**](csharelocknh--firstpartialtoexclusive.md) | Se usa para convertir un bloqueo parcial en un bloqueo exclusivo.         |
| [**PartialLock**](csharelocknh--partiallock.md)                         | Impide que más de un subproceso complete la adquisición de un bloqueo. |
| [**PartialUnlock**](csharelocknh--partialunlock.md)                     | Libera un bloqueo parcial.                                        |
| [**ShareLock**](csharelocknh--sharelock.md)                             | Obtiene un bloqueo para el modo compartido.                                 |
| [**ShareUnlock**](csharelocknh--shareunlock.md)                         | Libera un bloqueo del modo compartido.                               |
| [**SharedToPartial**](csharelocknh--sharedtopartial.md)                 | Obtiene un bloqueo parcial.                                         |
| [**TryExclusiveLock**](csharelocknh--tryexclusivelock.md)               | Obtiene un bloqueo exclusivamente.                                     |



 

 

 



