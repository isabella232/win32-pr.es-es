---
description: Un componente COM configurado normalmente se activa en su propio contexto; es decir, COM+ hace referencia a la información del catálogo de componentes para proporcionar los servicios configurados.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Aplicación de la activación en el contexto predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d188fb50521e09c88a9c61136e33928176faa1f70a94680b31cf0cc1e75cb8eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070765"
---
# <a name="enforcing-activation-in-the-default-context"></a>Aplicación de la activación en el contexto predeterminado

Un componente COM configurado normalmente se activa en su propio contexto; Es decir, COM+ hace referencia a la información del catálogo del componente para proporcionar los servicios configurados. Sin embargo, puede optar por activar un componente configurado en el contexto predeterminado. Un componente COM base,un componente registrado que no tiene información de catálogo de COM+, normalmente se activa en el contexto predeterminado.

La activación de un componente COM en el contexto predeterminado proporciona tres ventajas de rendimiento principales, como se muestra a continuación:

-   Los recursos del sistema se ahorran limitando el número de contextos que se crean.
-   Puede aumentar el rendimiento limitando el número de llamadas entre contextos. Dado que las llamadas entre contextos requieren serialización, es mucho más rápido que un objeto COM activado en el contexto predeterminado realice llamadas a otros objetos en el contexto predeterminado. El rendimiento en este caso (de las llamadas dentro del mismo contexto) es similar al de llamar a una subrutina.
-   Puede importar aplicaciones COM anteriores en COM+ y ejecutarlas sin ningún problema. Por ejemplo, puede tener varias aplicaciones COM anteriores implementadas bajo la suposición de que era posible pasar referencias de objeto dentro de un apartamento sin serializar las referencias. Estas aplicaciones COM no funcionan cuando se importan en COM+ porque las referencias de objeto se pasan a través de los límites de contexto. Sin embargo, puede hacer que este tipo de aplicación COM se ejecute cuando se importe si usa la herramienta administrativa Servicios de componentes para marcar todas las clases de la aplicación como Debe activarse en el **contexto predeterminado**.

La principal desventaja de activar un componente configurado en el contexto predeterminado es que COM+ no proporciona ninguno de los servicios configurados del componente. Hay un equilibrio entre el rendimiento mejorado y la capacidad de usar servicios COM+.

Por ejemplo, suponga que un componente COM no requiere ningún servicio COM+ (como Transacciones [,](com--transactions.md)Activación [Just-In-Time](com--just-in-time-activation.md), [Eventos](com--events.md) [,](com--queued-components.md)Componentes en [cola,](com--synchronization.md)Sincronización o Agrupación de [objetos)](com--object-pooling.md)y que el componente realiza una serie de llamadas a otros componentes COM que se pueden activar en el contexto predeterminado. En este caso, sería una buena idea activar el componente de llamada en el contexto predeterminado.

Si el componente COM requiere servicios COM+, no se puede marcar como **Debe activarse en el contexto predeterminado.** Además, no hay ninguna ganancia de rendimiento real si un objeto COM activado en el contexto predeterminado realiza una serie de llamadas a objetos en otros contextos. (Para obtener más detalles, vea [Contextos).](com--contexts.md)

**Para aplicar la activación en el contexto predeterminado**

1.  En el panel de detalles de la herramienta administrativa Servicios  de componentes, haga clic con el botón derecho en el componente (ubicado dentro de la carpeta Componentes de cualquier aplicación COM+ seleccionada) que quiera activar en el contexto predeterminado y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo Propiedades del componente, haga clic en **la pestaña** Activación.

3.  Active la **casilla Must be activated in the default context**(Debe activarse en el contexto predeterminado).

4.  Haga clic en **Aceptar**.

> [!Note]  
> Cuando se ejecuta un componente configurado en el contexto predeterminado, COM+ no activa ninguno de los servicios configurados para ese componente. Estos servicios están disponibles de nuevo al desactivar la casilla Debe activarse en el contexto predeterminado y, posteriormente, ejecutar el componente configurado en su propio contexto.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-In-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aplicación de la activación en el contexto del autor de la llamada](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



