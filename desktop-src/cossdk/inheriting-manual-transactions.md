---
description: Heredar transacciones manuales
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Heredar transacciones manuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465775"
---
# <a name="inheriting-manual-transactions"></a>Heredar transacciones manuales

Si un objeto con una transacción BYOT en su contexto crea un segundo objeto, el objeto de nivel inferior puede heredar la transacción BYOT (si está configurada para heredar transacciones). El primer objeto creado mediante la puerta de enlace BYOT debe configurarse para "requerir" o "admitir" transacciones. Los objetos posteriores de la actividad se podrían configurar en función de los requisitos de la aplicación.

En el caso de las transacciones automáticas, el tiempo de ejecución de COM+ no intenta confirmar la transacción hasta que el objeto raíz indica que está lista (llamando a [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) antes de volver de una llamada). Los usuarios deben tener en cuenta que una transacción BYOT podría confirmarse prematuramente (en el caso de que no se haya completado el trabajo de los objetos secundarios), porque la "raíz" no se ejecuta en el entorno en tiempo de ejecución de COM+ y la semántica de confirmación no está asociada a la duración del objeto. En general, el usuario debe tener cuidado de no infringir el límite de sincronización de la transacción.

De lo contrario, se aplica la semántica de confirmación de COM+. COM+ no intentará confirmar una transacción mientras se llama a un objeto dentro de un límite de sincronización. Además, los objetos pueden indicar su coherencia mediante [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit). Si se intenta confirmar una transacción que incluye el trabajo de un objeto llamado **DisableCommit**, la transacción se anulará.

 

 



