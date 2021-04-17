---
description: El atributo de sincronización es una propiedad declarativa que especifica el tipo de sincronización que desea que tengan los componentes cuando se activan.
ms.assetid: 7f044ee5-b99e-4f0c-a680-b1e2672949fc
title: Valores de atributo de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4606726d5202a1453e98d5bf609084982f8f824e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423311"
---
# <a name="synchronization-attribute-values"></a>Valores de atributo de sincronización

El atributo de sincronización es una propiedad declarativa que especifica el tipo de sincronización que desea que tengan los componentes cuando se activan. Al incluir el atributo de sincronización, COM+ controla los detalles de la sincronización en su nombre. no es necesario realizar ninguna otra llamada.

En función de sus requisitos, un objeto puede compartir la sincronización del autor de la llamada, requerir una nueva sincronización o funcionar sin sincronización.

COM+ proporciona los siguientes valores de atributo de sincronización:

-   **Deshabilitado.** Al deshabilitar el atributo de sincronización, COM+ omite los requisitos de sincronización del componente para determinar el contexto del objeto. Como resultado, el objeto puede o no compartir el contexto del autor de la llamada (y la sincronización).

    En general, debe usar este valor de atributo cuando sepa que el componente nunca accede a un administrador de recursos. Al migrar componentes COM a COM+, debe deshabilitar el atributo de sincronización para mantener el mismo comportamiento que el componente COM sin configurar. Un componente sin configurar es un componente COM que no se ha instalado en una aplicación COM+.

-   **No compatible.** Un objeto con este valor nunca participa en la sincronización, independientemente del estado de su llamador. Esta opción solo está disponible para los componentes que no son transaccionales y no utilizan el servicio de [activación Just-in-Time (JIT) de com+](com--just-in-time-activation.md) .

-   **Realizar.** Un objeto con este valor participa en la sincronización si existe. Este valor se declara cuando se desea que un objeto se comparta en la sincronización del llamador, pero no se requiere la sincronización propia.

    Una buena razón para establecer el atributo de sincronización en compatible es que esta configuración puede ser más económica en cuanto a recursos del sistema. Sin embargo, es más difícil escribir el componente debido a la necesidad de protegerlo de llamadas simultáneas. La implicación de establecer el atributo de sincronización en compatible es que, en determinadas circunstancias, se puede crear una instancia del objeto de manera que no esté sincronizada. Si el modelo de subprocesos del componente es gratuito o ambos, tendrá que proteger los datos de instancia con algún tipo de mecanismo de bloqueo. Si el modelo de subprocesos es apartamento (STA), no tendrá que proteger los datos de la instancia.

-   **Obligatorio.** Al establecer este atributo, COM+ garantiza que todos los objetos creados a partir del componente se sincronizarán. En efecto, siempre que COM+ crea una instancia del componente, se asegura de que solo haya un subproceso a través de esta instancia a la vez.

    Cuando COM+ activa un objeto, examina el estado de sincronización de su llamador. Si el llamador está sincronizado, COM+ transfiere el límite de sincronización del llamador para incluir el nuevo objeto. De lo contrario, COM+ inicia la sincronización.

-   **Requiere un nuevo.** Un objeto con este valor debe participar en una nueva sincronización, donde COM+ administra los contextos y apartamentos en nombre de todos los componentes implicados en la llamada. COM+ inicia automáticamente una nueva sincronización, que es distinta de la sincronización del llamador.

    Una buena razón para establecer el atributo de sincronización en requires New es que esta configuración permite realizar llamadas externas a una instancia del componente de forma más eficaz. Sin embargo, también realiza llamadas entre el objeto y el objeto que lo creó más caro en cuanto a recursos del sistema.

    Por ejemplo, Imagine un caso en el que el objeto y su objeto Creator comparten el mismo límite de sincronización. Si el cliente A llama al objeto Creator y el cliente B llama a su objeto, la segunda llamada tendrá que esperar hasta que se complete la primera llamada. Si establece requires New, el objeto se crea en un límite de sincronización independiente. En este caso, las llamadas de otros objetos pueden procesarse al mismo tiempo. Sin embargo, las llamadas del objeto Creator al objeto requieren más recursos del sistema porque deben cruzar los límites de sincronización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer el atributo de sincronización](setting-the-synchronization-attribute.md)
</dt> <dt>

[Dependencias de sincronización](synchronization-dependencies.md)
</dt> </dl>

 

 



