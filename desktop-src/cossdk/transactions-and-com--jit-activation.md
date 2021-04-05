---
description: Transacciones y activación JIT de COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transacciones y activación JIT de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907441"
---
# <a name="transactions-and-com-jit-activation"></a>Transacciones y activación JIT de COM+

La activación JIT de COM+ está estrechamente enlazada a transacciones automáticas. Cuando se configura un componente para que requiera una transacción o se requiera una nueva transacción, la activación JIT también se habilita automáticamente. Las dos características funcionan de forma natural en conjunción. Los componentes transaccionales y activados en JIT comparten las siguientes características:

-   Estados. No contendría el estado que infringiría el aislamiento de transacción ni contenía el estado que se perdería en la desactivación de objetos.

-   Uso rápido. El patrón de uso canónico para un objeto que realiza el trabajo en una transacción automática consiste en realizar una pequeña unidad de trabajo, votación y salida.

    > [!Note]  
    > Las formas de votar en las transacciones COM+ y la realización de señales para la activación JIT también están estrechamente enlazadas. Para obtener más información, vea [establecer el bit Done](setting-the-done-bit.md).

     

-   Uso repetido. Cuando el trabajo transaccional se ha dividido correctamente, los clientes utilizan los mismos objetos una y otra vez para realizar pocas parcelas de trabajo atómico.

-   Desactivado al confirmar o anular. En COM+, todos los objetos dentro del límite de la transacción se desactivan cuando la transacción se confirma o se anula.

Junto con los componentes transaccionales de COM+, la activación JIT sirve como una mejora de gran rendimiento al mantener el canal abierto como los clientes contienen referencias de larga duración a objetos transaccionales. Como mejora adicional, puede agrupar los objetos transaccionales para reutilizar los recursos que contienen, acelerar el tiempo de reactivación de objetos y administrar de cerca cómo se usan los recursos de memoria para los objetos especificados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-in-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitar la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Agrupación de objetos y activación JIT de COM+](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



