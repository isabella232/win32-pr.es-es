---
description: Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Escribir un Administrador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677690"
---
# <a name="writing-a-resource-manager"></a>Escribir un Administrador de recursos

Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).

Para escribir un administrador de recursos, debe crear varios objetos de kernel. Los objetos que usa un RM son:

-   Objetos del administrador de transacciones (TM)
-   Objetos Administrador de recursos
-   Objetos de inscripción

En primer lugar, cree un objeto TM. Hay dos tipos de TM:

-   Volatile: estas TM no tienen un registro y no pueden recuperar su estado
-   Durable: estas TM tienen un registro

Para crear un TM duradero, debe crear un registro de CLFS y llamar a [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) o hacer que KTM lo cree. Después de crear un TM duradero, primero debe recuperar el TM llamando a [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager). Una vez recuperado el TM, está disponible para su uso.

Si ha recuperado un TM existente, todos los RMs asociados a este TM comenzarán a recibir los mensajes de recuperación. Para obtener más información, vea [procesamiento de recuperación](recovery-processing.md).

A continuación, cree un administrador de recursos mediante una llamada a [**CreateResourceManager (**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) con el identificador de TM. RM puede ser volátil o durable. Solo se puede usar TM durable con RMs duradero.

Al trabajar de forma transaccional, se da de alta en la transacción llamando a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)y especificando qué notificaciones se van a recibir.

**Nota:**  Puede empezar a recibir notificaciones antes de que se complete la llamada a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) .

Cuando reciba una notificación, llame a la función "Complete \* " adecuada cuando se complete cualquier trabajo asociado al procesamiento de la notificación. Las funciones completas son:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Si, en algún momento, un administrador de recursos no puede completar el trabajo de la transacción, o si continúa, la aplicación no puede deshacer el trabajo realizado dentro de la transacción, debe revertir la transacción llamando a [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



