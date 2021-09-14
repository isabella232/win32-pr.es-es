---
description: En el modelo de programación COM+, puede diseñar los componentes para hacer lo que mejor hacen&8212; habilitar la lógica de negocios o establecer una conexión de base de datos \#&8212; y confiar en el marco de procesamiento de transacciones de Microsoft Windows para automatizar las \# transacciones.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Administración de transacciones automáticas en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361678"
---
# <a name="managing-automatic-transactions-in-com"></a>Administración de transacciones automáticas en COM+

En el modelo de programación COM+, puede diseñar los componentes para hacer lo que mejor hacen (habilitar la lógica de negocios o establecer una conexión de base de datos) y confiar en el marco de procesamiento de transacciones de Microsoft Windows para automatizar las transacciones.

## <a name="starting-a-transaction"></a>Iniciar una transacción

COM+ inicia automáticamente una transacción cuando encuentra cualquiera de las condiciones siguientes:

-   Cuando un cliente no transaccional llama a un componente que requiere una transacción o requiere una nueva transacción.
-   Cuando un cliente transaccional llama a un componente que requiere una nueva transacción.

Si COM+ determina que un objeto debe tener una nueva transacción, primero comienza la transacción y, a continuación, coloca el objeto en él. El proceso consta de los pasos siguientes:

1.  COM+ crea un objeto de contexto, [](com--synchronization.md) establece los atributos activación [JIT](com--just-in-time-activation.md) y Sincronización en Requerido y establece las marcas coherentes y [realizadas](consistent-and-done-flags.md) en True y False, respectivamente.
2.  COM+ se comunica con el Coordinador de transacciones distribuidas (DTC) para iniciar una transacción. El DTC coordina la transacción física.
3.  El DTC genera un identificador de transacción y lo vuelve a pasar a COM+. El identificador de transacción establece un límite de transacción. Todos los objetos que participan en la transacción comparten el mismo identificador.
4.  Cuando el cliente crea el objeto, COM+ lo activa dentro del límite de transacción.

## <a name="ending-a-transaction"></a>Finalización de una transacción

COM+ finaliza una transacción automática confirmando o anulando cuando se produce una de las condiciones siguientes:

-   El objeto raíz de la transacción completa su trabajo y COM+ lo libera. Una vez que se desactiva el objeto raíz, la transacción intenta confirmarse.
-   El cliente libera el objeto raíz. Sin una referencia, el objeto raíz se desactiva y la transacción intenta confirmarse.
-   La transacción supera su umbral de tiempo de espera. La transacción se anula automáticamente si no se confirma dentro del período de tiempo de espera de la transacción, desactivando todos los objetos asociados a la transacción. El período de tiempo de espera predeterminado de la transacción es de 60 segundos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Marcas coherentes y realizadas](consistent-and-done-flags.md)
</dt> <dt>

[Acelerar transacciones notificando al objeto raíz](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[Terminación de una transacción automática mediante una llamada a SetComplete](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



