---
description: Transacciones y activación JIT de COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transacciones y activación JIT de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2b496f46652dc8ab9f6d573e712a0aa83575cac0adbb86a7dc4cfa88b565ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546052"
---
# <a name="transactions-and-com-jit-activation"></a>Transacciones y activación JIT de COM+

La activación JIT de COM+ está estrechamente enlazada a las transacciones automáticas. Al configurar un componente para que requiera una transacción o requiera una nueva transacción, la activación JIT también se habilita automáticamente. Las dos características funcionan de forma natural juntos. Los componentes transaccionales activados JIT comparten las siguientes características:

-   Apatridia. No tendría el estado que infringiría el aislamiento de transacción ni el estado que se perdería al desactivar el objeto.

-   Uso rápido. El patrón de uso canónico para un objeto que realiza el trabajo en una transacción automática es realizar una pequeña unidad de trabajo, votar y salir.

    > [!Note]  
    > Las maneras de votar en transacciones COM+ y el hecho de señalar la activación JIT también se enlazan estrechamente. Para obtener más información, [vea Establecer el bit listo.](setting-the-done-bit.md)

     

-   Uso repetido. Cuando el trabajo transaccional se divide correctamente, los clientes usan los mismos objetos una y otra vez para realizar pequeñas tareas de trabajo atómico.

-   Desactivado al confirmar o anular. En COM+, todos los objetos dentro del límite de transacción se desactivan cuando la transacción se confirma o anula.

Junto con los componentes transaccionales de COM+, la activación JIT sirve como una gran mejora del rendimiento al mantener el canal abierto, ya que los clientes mantienen referencias de larga duración a objetos transaccionales. Como mejoras adicionales, puede optar por agrupar los objetos transaccionales para reutilizar los recursos que contiene, acelerar el tiempo de reactivación de objetos y administrar estrechamente cómo se usan los recursos de memoria para objetos determinados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-In-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitación de la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Agrupación de objetos y activación JIT de COM+](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



