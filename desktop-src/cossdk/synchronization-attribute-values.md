---
description: El atributo synchronization es una propiedad declarativa que especifica qué tipo de sincronización desea que tengan los componentes cuando se activen.
ms.assetid: 7f044ee5-b99e-4f0c-a680-b1e2672949fc
title: Valores de atributo de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4606726d5202a1453e98d5bf609084982f8f824e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361630"
---
# <a name="synchronization-attribute-values"></a>Valores de atributo de sincronización

El atributo synchronization es una propiedad declarativa que especifica qué tipo de sincronización desea que tengan los componentes cuando se activen. Al incluir el atributo de sincronización, COM+ controla los detalles de la sincronización en su nombre; no es necesario realizar ninguna otra llamada.

En función de sus requisitos, un objeto puede compartir la sincronización de su autor de la llamada, requerir una nueva sincronización o funcionar sin sincronización.

COM+ proporciona los siguientes valores de atributo de sincronización:

-   **Deshabilitado.** Al deshabilitar el atributo de sincronización, COM+ omite los requisitos de sincronización del componente para determinar el contexto del objeto. Como resultado, el objeto puede compartir o no el contexto (y la sincronización) del autor de la llamada.

    En general, debe usar este valor de atributo cuando sepa que el componente nunca accede a un administrador de recursos. Al migrar componentes COM a COM+, debe deshabilitar el atributo de sincronización para mantener el mismo comportamiento que el componente COM no configurado. Un componente no configurado es un componente COM que no se ha instalado en una aplicación COM+.

-   **No compatible** Un objeto con este valor nunca participa en la sincronización, independientemente del estado de su llamador. Esta configuración solo está disponible para los componentes que no son transaccionales y no usan el servicio de activación [Just-In-Time (JIT)](com--just-in-time-activation.md) de COM+.

-   **Compatible.** Un objeto con este valor participa en la sincronización si existe. Este valor se declara cuando se desea que un objeto comparta la sincronización de su autor de la llamada, pero no se requiere su propia sincronización.

    Una buena razón para establecer el atributo de sincronización en Compatible es que esta configuración puede ser menos costosa en términos de recursos del sistema. Sin embargo, es más difícil escribir el componente debido a la necesidad de protegerlo frente a llamadas simultáneas. La implicación de establecer el atributo de sincronización en Compatible es que, en determinadas circunstancias, se puede crear una instancia del objeto de forma que no esté sincronizada. Si el modelo de subprocesos del componente es Gratis o Ambos, tendrá que proteger los datos de la instancia con algún tipo de mecanismo de bloqueo. Si el modelo de subprocesos es Apartment (STA), no tendrá que proteger los datos de la instancia.

-   **Requerido.** Al establecer este atributo, COM+ garantiza que se sincronizarán todos los objetos creados a partir del componente. En efecto, cada vez que COM+ crea una instancia del componente, se asegura de que solo haya un subproceso que pase por esta instancia a la vez.

    A medida que COM+ activa un objeto, examina el estado de sincronización de su autor de la llamada. Si el autor de la llamada está sincronizado, COM+ fluye el límite de sincronización del autor de la llamada para incluir el nuevo objeto. De lo contrario, COM+ inicia la sincronización.

-   **Requiere Nuevo.** Un objeto con este valor debe participar en una nueva sincronización, donde COM+ administra contextos y departamentos en nombre de todos los componentes implicados en la llamada. COM+ inicia automáticamente una nueva sincronización, que es distinta de la sincronización del autor de la llamada.

    Una buena razón para establecer el atributo de sincronización en Requiere nuevo es que esta configuración le permite realizar llamadas externas a una instancia del componente de forma más eficaz. Sin embargo, también realiza llamadas entre el objeto y el objeto que lo creó más caro en términos de recursos del sistema.

    Por ejemplo, suponga un caso en el que el objeto y su objeto creator comparten el mismo límite de sincronización. Si el cliente A llama al objeto creator y el cliente B llama al objeto , la segunda llamada tendrá que esperar hasta que se complete la primera llamada. Si establece Requiere nuevo, el objeto se crea en un límite de sincronización independiente. En este caso, las llamadas desde otros objetos se pueden procesar al mismo tiempo. Sin embargo, las llamadas desde el objeto creator al objeto requieren más recursos del sistema porque deben cruzar los límites de sincronización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer el atributo de sincronización](setting-the-synchronization-attribute.md)
</dt> <dt>

[Dependencias de sincronización](synchronization-dependencies.md)
</dt> </dl>

 

 



