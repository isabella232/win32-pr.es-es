---
description: Cuando un objeto se activa en un contexto determinado, las llamadas subsiguientes a o desde él, dentro del contexto, se tratan de manera diferente que las llamadas en el límite del contexto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interceptación de llamadas entre contextos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360051"
---
# <a name="interception-of-cross-context-calls"></a>Interceptación de llamadas entre contextos

Cuando un objeto se activa en un contexto determinado, las llamadas subsiguientes a o desde él, dentro del contexto, se tratan de manera diferente que las llamadas en el límite del contexto. Las llamadas en el límite del contexto se administran con servidores proxy ligeros. Estos proxies controlan cualquier mediación necesaria para ajustar el entorno en tiempo de ejecución desde uno que admita al llamador a uno que se acomode al destinatario. Este proceso se conoce como *intercepción*.

La intercepción de llamadas entre contextos es necesaria porque los objetos de contextos diferentes tienen requisitos de tiempo de ejecución diferentes, es precisamente el motivo de los contextos. COM+ intercepta las referencias a objetos que se pasan como parámetros de método y las convierte automáticamente en servidores proxy para que se puedan usar en el nuevo contexto.

Si comparte referencias a objetos entre los límites del contexto por otros medios (por ejemplo, en variables globales) siempre debe usar [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) y [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). Estas funciones pueden traducir una referencia de objeto en un proxy que se puede usar en un contexto diferente. Nunca comparta una referencia de objeto sin formato a través de los límites del contexto.

El comportamiento de las llamadas en el contexto puede tener consecuencias no deseadas en el caso de los objetos que exponen interfaces en las que no se pueden calcular las referencias. En este caso, es probable que desee insistir en que el objeto al que no se pueden calcular las referencias se active solo en el contexto de su llamador y nunca en su propio contexto. Para ello, seleccione la opción **debe activarse en el contexto del autor** de la llamada en la pestaña **activación** de la página **propiedades** del componente. (Vea [forzar la activación en el contexto del autor de la llamada](enforcing-activation-in-the-caller-s-context.md) para obtener instrucciones paso a paso).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Activación de contexto](context-activation.md)
</dt> </dl>

 

 
