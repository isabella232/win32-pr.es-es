---
description: En el modelo de programación COM+, puede diseñar los componentes para hacer lo que mejor&\# 8212; habilitar la lógica de negocios o establecer una conexión de base de datos&\# 8212; y basarse en el marco de procesamiento de transacciones de Microsoft Windows para automatizar las transacciones.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Administrar transacciones automáticas en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539195"
---
# <a name="managing-automatic-transactions-in-com"></a>Administrar transacciones automáticas en COM+

En el modelo de programación de COM+, puede diseñar los componentes para hacer lo que mejor se adapte a la lógica de negocios o al establecer una conexión de base de datos, y basarse en el marco de procesamiento de transacciones de Microsoft Windows para automatizar las transacciones.

## <a name="starting-a-transaction"></a>Iniciar una transacción

COM+ inicia automáticamente una transacción cuando encuentra cualquiera de las siguientes condiciones:

-   Cuando un cliente no transaccional llama a un componente que requiere una transacción o requiere una nueva transacción.
-   Cuando un cliente transaccional llama a un componente que requiere una nueva transacción.

Si COM+ determina que un objeto debe tener una nueva transacción, comienza primero la transacción y, a continuación, coloca el objeto en ella. El proceso consta de los pasos siguientes:

1.  COM+ crea un objeto de contexto, establece los atributos de [activación](com--just-in-time-activation.md) y [sincronización](com--synchronization.md) JIT en Required y establece las [marcas coherente y](consistent-and-done-flags.md) final en true y false, respectivamente.
2.  COM+ se comunica con el Coordinador de transacciones distribuidas (DTC) para iniciar una transacción. El DTC coordina la transacción física.
3.  El DTC genera un identificador de transacción y lo pasa de nuevo a COM+. El identificador de transacción establece un límite de transacción. Todos los objetos que participan en la transacción comparten el mismo identificador.
4.  Cuando el cliente crea el objeto, COM+ lo activa en el límite de la transacción.

## <a name="ending-a-transaction"></a>Finalizar una transacción

COM+ finaliza una transacción automática mediante la confirmación o la anulación cuando se produce una de las siguientes condiciones:

-   El objeto raíz de la transacción completa su trabajo y COM+ lo libera. Una vez desactivado el objeto raíz, la transacción intenta confirmarse.
-   El cliente libera el objeto raíz. Sin una referencia, el objeto raíz se desactiva y la transacción intenta confirmarse.
-   La transacción supera el umbral de tiempo de espera. La transacción se anula automáticamente si no se confirma en el período de tiempo de espera de la transacción, desactivando todos los objetos asociados a la transacción. El período de tiempo de espera predeterminado de la transacción es de 60 segundos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Marcas de coherencia y de realización](consistent-and-done-flags.md)
</dt> <dt>

[Acelerar las transacciones mediante la notificación del objeto raíz](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[Finalizar una transacción automática llamando a SetComplete](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



