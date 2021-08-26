---
description: Establecer el bit listo
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Establecer el bit listo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad2d9a9dc06caa623d3f7c58d51aec389b40a1f3315ae09a21052bdf6e2ae3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070255"
---
# <a name="setting-the-done-bit"></a>Establecer el bit listo

COM+ desactivará un objeto activado JIT en función del estado de una propiedad de contexto, el bit listo, como se muestra a continuación:

-   Cuando el bit terminado se establece en True, COM+ desactiva el objeto cuando se devuelve la llamada al método actual.
-   Cuando el bit terminado se establece en False, el objeto permanece activo cuando se devuelve la llamada al método actual.

De forma predeterminada, el bit terminado se establece en False cuando se crea un objeto y se inicializa su contexto. (Cualquier objeto activado JIT se crea en su propio contexto para que tenga su propio bit listo para establecer). Sin embargo, puede cambiar esta configuración predeterminada por método mediante la propiedad auto-done. Puede establecer el bit listo de las maneras siguientes:

-   Uso [ **de IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Uso [ **de IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Uso de la propiedad auto-done

## <a name="using-icontextstate"></a>Uso de IContextState

Puede usar [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) para establecer el bit listo en True o False.

Puede usar [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) para obtener el estado actual del bit listo del contexto del objeto.

## <a name="using-iobjectcontext"></a>Uso de IObjectContext

Puede usar los métodos siguientes en [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para establecer el bit listo mientras se establece simultáneamente el bit coherente utilizado para votar en transacciones:

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) indica que ha terminado y que vota para confirmar la transacción actual. Establece el bit listo y el bit coherente en True.
-   [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) indica que ha terminado y desmón la transacción actual. Establece el bit listo en True y el bit coherente en False.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) indica que no ha terminado, pero que vota para confirmar la transacción. Establece el bit realizado en False y el bit coherente en True.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) indica que no ha terminado y que vota no confirmar la transacción en este momento, normalmente porque el estado es incoherente. Establece el bit listo y el bit coherente en False.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-In-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitación de la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Agrupación de objetos y activación JIT de COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transacciones y activación JIT de COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



