---
description: Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Escribir un Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b1443bef61f56a14779612a6275aacbd65e344d7294325bd87b953795f0f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086455"
---
# <a name="writing-a-resource-manager"></a>Escribir un Resource Manager

Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).

Para escribir un administrador de recursos, debe crear varios objetos de kernel. Los objetos que usa un RM son:

-   Objetos del Administrador de transacciones (TM)
-   Resource Manager objetos
-   Enlistment objects (Objetos de registro)

En primer lugar, cree un objeto TM. Hay dos tipos de MÁQUINAS virtuales:

-   Volátil: estas máquinas virtuales no tienen un registro y no pueden recuperar su estado.
-   Durable: estos TMs tienen un registro

Para crear una TM duradera, debe crear un registro CLFS y llamar a [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) o hacer que KTM lo cree de forma automática. Después de crear una TM duradera, primero debe recuperar la TM mediante una llamada a [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager). Una vez recuperado el TM, está disponible para su uso.

Si ha recuperado una TM existente, todos los RMs asociados a esta TM comenzarán a recibir mensajes de recuperación. Para obtener más información, vea [Procesamiento de recuperación.](recovery-processing.md)

A continuación, cree un administrador de recursos mediante una [**llamada a CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) con el identificador tm. El RM puede ser volátil o duradero. Solo se pueden usar máquinas virtuales durables con RMs duraderos.

Cuando se trabaja transaccionalmente, se insinte en la transacción llamando a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)y especificando qué notificaciones recibir.

**Nota**  Puede empezar a recibir notificaciones antes de que se complete la llamada a [**CreateEnlistment.**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)

Cuando reciba una notificación, llame a la función "Complete" adecuada cuando se complete cualquier trabajo asociado con el procesamiento \* de la notificación. Las funciones completas son:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Si en algún momento un administrador de recursos no puede completar el trabajo de la transacción o si continuar podría hacer que la aplicación no pueda deshacer el trabajo realizado dentro de la transacción, debe revertir la transacción llamando a [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



