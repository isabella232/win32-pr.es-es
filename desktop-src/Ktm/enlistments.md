---
description: Un administrador de recursos se da de alta en una transacción cuando comienza la participación en esa transacción concreta.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Inscripciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52820af2a7b280bc4740d0309fb627725e648685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279014"
---
# <a name="enlistments"></a>Inscripciones

Un administrador de recursos se da de alta en una transacción cuando comienza la participación en esa transacción concreta. La inscripción define las notificaciones que el administrador de recursos acepta. Un administrador de recursos crea un objeto de inscripción cuando se da de alta en una transacción. Este objeto señala a KTM que el administrador de recursos (RM) solicita notificaciones sobre la transacción especificada.

RM proporciona una estructura [**de \_ máscara de notificación**](notification-mask.md) que detalla las notificaciones que solicita.

## <a name="enlistment-functions"></a>Funciones de inscripción

Las siguientes funciones se usan con inscritos.



| Función                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que un administrador de recursos (RM) ha terminado de confirmar una transacción solicitada por el administrador de transacciones (TM).                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea una inscripción, establece su estado inicial y abre un identificador para la inscripción con el acceso especificado.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una estructura opaca de datos de recuperación de KTM. La información de recuperación se almacena en un inicio de sesión en nombre de un administrador de recursos (RM) mediante una llamada a la función [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . Después de un error, el RM puede usar la función [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre un objeto de inscripción existente y devuelve un identificador a la inscripción.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que la inscripción especificada se convierta en una inscripción de solo lectura. Una inscripción de solo lectura no puede participar en el resultado de la transacción y no se registra de forma duradera para la recuperación.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Revierte la transacción especificada que está asociada a una inscripción. No se puede llamar a esta función para las inlistas de solo lectura.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Establece una estructura opaca definida por el usuario de los datos de recuperación de KTM. La información de recuperación se almacena en un inicio de sesión en nombre de un administrador de recursos (RM) mediante una llamada a [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Después de un error, el RM puede usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que el administrador de recursos (RM) rechaza una solicitud de una sola fase. Cuando un administrador de transacciones (TM) recibe esta llamada, inicia una confirmación en dos fases y envía una solicitud de preparación a todo el RMs dado de alta.                                                                                                                                                                                       |



 

 

 



