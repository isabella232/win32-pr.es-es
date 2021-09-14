---
description: Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Escribir un Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160013"
---
# <a name="writing-a-resource-manager"></a>Escribir un Resource Manager

Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).

Para escribir un administrador de recursos, debe crear varios objetos de kernel. Los objetos que usa un RM son:

-   Objetos del Administrador de transacciones (TM)
-   Resource Manager objetos
-   Objetos de alta

En primer lugar, cree un objeto TM. Hay dos tipos de máquinas virtuales:

-   Volatile: estos TMs no tienen un registro y no pueden recuperar su estado.
-   Durable: estas máquinas virtuales tienen un registro

Para crear una TM durable, debe crear un registro CLFS y llamar a [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) o hacer que KTM lo cree de forma automática. Después de crear una TM duradera, primero debe recuperar la TM mediante una llamada a [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager). Una vez recuperado el TM, está disponible para su uso.

Si recuperó una TM existente, todos los RMs asociados a esta TM comenzarán a recibir mensajes de recuperación. Para obtener más información, vea [Procesamiento de recuperación.](recovery-processing.md)

A continuación, cree un administrador de recursos mediante una [**llamada a CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) con el identificador de TM. El RM puede ser volátil o duradero. Solo se pueden usar máquinas virtuales durables con RMs duraderos.

Al trabajar transaccionalmente, para dar de alta en la transacción, llame a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)y especifique las notificaciones que se recibirán.

**Nota**  Puede empezar a recibir notificaciones antes de que se complete la llamada a [**CreateEnlistment.**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)

Cuando reciba una notificación, llame a la función "Complete" adecuada cuando se complete cualquier trabajo asociado con el procesamiento \* de la notificación. Las funciones completas son:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Si en algún momento un administrador de recursos no puede completar el trabajo de la transacción, o si continuar haría que la aplicación no pudiera deshacer el trabajo realizado dentro de la transacción, debe revertir la transacción llamando a [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



