---
description: Grupo de métodos que se usa para manipular bloqueos.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Métodos CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659453"
---
# <a name="csharelocknh-methods"></a>Métodos CShareLockNH

Grupo de métodos que se usa para manipular bloqueos.

## <a name="methods"></a>Métodos

A continuación se muestran los métodos exportados por Rwnh.dll.



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



 

 

 



