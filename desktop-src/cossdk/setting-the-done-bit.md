---
description: Establecer el bit Done
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Establecer el bit Done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705358"
---
# <a name="setting-the-done-bit"></a>Establecer el bit Done

COM+ desactivará un objeto activado en JIT en función del estado de una propiedad de contexto, el bit Done, como se indica a continuación:

-   Cuando el bit Done está establecido en true, COM+ desactiva el objeto cuando se devuelve la llamada al método actual.
-   Cuando el bit Done está establecido en false, el objeto permanece activo cuando se devuelve la llamada al método actual.

De forma predeterminada, el bit done se establece en false cuando se crea un objeto y se inicializa su contexto. (Cualquier objeto activado en JIT se crea en su propio contexto para que tenga su propio bit de finalización). Sin embargo, puede cambiar esta configuración predeterminada en función de cada método mediante la propiedad auto-done. Puede establecer el bit Done de las maneras siguientes:

-   Usar [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Usar [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Usar la propiedad auto-Done

## <a name="using-icontextstate"></a>Usar IContextState

Puede usar [**IContextState:: SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) para establecer el bit done en true o false.

Puede usar [**IContextState:: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) para obtener el estado actual del bit Done desde el contexto del objeto.

## <a name="using-iobjectcontext"></a>Usar IObjectContext

Puede usar los métodos siguientes en [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para establecer el bit Done mientras configura simultáneamente el bit coherente que se usa para votar en transacciones:

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) indica que ha terminado y que ha votado para confirmar la transacción actual. Establece el bit Done y el bit coherente en true.
-   El [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) indica que ha terminado y termina la transacción actual. Establece el bit done en true y el bit coherente en false.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) señala que no ha terminado pero que ha votado para confirmar la transacción. Establece el bit done en false y el bit coherente en true.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) indica que no está listo y que vota no confirmar la transacción en este momento, normalmente porque el estado es incoherente. Establece el bit Done y el bit coherente en false.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-in-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitar la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Agrupación de objetos y activación JIT de COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transacciones y activación JIT de COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



