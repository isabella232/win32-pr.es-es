---
description: Heredar transacciones manuales
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Heredar transacciones manuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705263"
---
# <a name="inheriting-manual-transactions"></a>Heredar transacciones manuales

Si un objeto con una transacción de transacciones manuales en su contexto crea un segundo objeto, el objeto de nivel inferior puede heredar la transacción de transacciones de transacciones (si se configura para que herede transacciones). El primer objeto creado mediante la puerta de enlace de transacciones se debe configurar para "requerir" o "admitir" transacciones. Los objetos subsiguientes de la actividad se pueden configurar en función de los requisitos de la aplicación.

En el caso de las transacciones automáticas, el tiempo de ejecución de COM+ no intenta confirmar la transacción hasta que el objeto raíz indica que está preparada (llamando a [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) antes de volver de una llamada). Los usuarios deben tener en cuenta que una transacción de transacciones se puede confirmar prematuramente (en el caso de que no se haya completado el trabajo de los objetos secundarios), ya que la "raíz" no se está ejecutando en el entorno de tiempo de ejecución de COM+ y la semántica de confirmación no está asociada a la duración del objeto. En general, el usuario debe tener cuidado de no infringir el límite de sincronización de la transacción.

De lo contrario, se aplica la semántica de confirmación de COM+. COM+ no intentará confirmar una transacción mientras un objeto dentro de un límite de sincronización está llamando a. Además, los objetos pueden indicar su coherencia mediante [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit). Si se intenta confirmar una transacción que incluye el trabajo de un objeto que ha llamado a **DisableCommit**, se anulará la transacción.

 

 



