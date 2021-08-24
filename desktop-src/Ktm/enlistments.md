---
description: Un administrador de recursos se da de alta en una transacción cuando comienza la participación en esa transacción determinada.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Alistamientos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19fea9c19da9bb16f81bd417e22c943876997ac224e3823020e5660218dfa5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146589"
---
# <a name="enlistments"></a>Alistamientos

Un administrador de recursos se da de alta en una transacción cuando comienza la participación en esa transacción determinada. La lista define qué notificaciones acepta el administrador de recursos. Un administrador de recursos crea un objeto de registro cuando se da de alta en una transacción. Este objeto indica a KTM que el administrador de recursos (RM) solicita notificaciones sobre la transacción especificada.

Rm proporciona una [**estructura NOTIFICATION \_ MASK**](notification-mask.md) que detalla las notificaciones que solicita.

## <a name="enlistment-functions"></a>Funciones de alta

Las siguientes funciones se usan con las inscciones.



| Función                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que un administrador de recursos (RM) ha terminado de confirmar una transacción solicitada por el administrador de transacciones (TM).                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea una lista, establece su estado inicial y abre un identificador para la alta con el acceso especificado.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una estructura opaca de datos de recuperación de KTM. La información de recuperación se almacena en un registro en nombre de un administrador de recursos (RM) mediante una llamada a la [**función SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Después de un error, rm puede usar la [**función GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre un objeto de registro existente y devuelve un identificador a la lista.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que la lista especificada se convierta en una lista de solo lectura. Una alta de solo lectura no puede participar en el resultado de la transacción y no se registra de forma dura para la recuperación.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Revierte la transacción especificada que está asociada a una alta. No se puede llamar a esta función para las inselecciones de solo lectura.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Establece una estructura opaca definida por el usuario de los datos de recuperación de KTM. La información de recuperación se almacena en un registro en nombre de un administrador de recursos (RM) mediante una llamada a [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Después de un error, rm puede usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que el administrador de recursos (RM) rechaza una solicitud de una sola fase. Cuando un administrador de transacciones (TM) recibe esta llamada, inicia una confirmación en dos fases y envía una solicitud de preparación a todos los RMs inscritos.                                                                                                                                                                                       |



 

 

 



