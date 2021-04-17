---
description: Un componente COM configurado normalmente se activa en su propio contexto; es decir, COM+ hace referencia a la información del catálogo de componentes para proporcionar los servicios configurados.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Forzar la activación en el contexto predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539424"
---
# <a name="enforcing-activation-in-the-default-context"></a>Forzar la activación en el contexto predeterminado

Un componente COM configurado normalmente se activa en su propio contexto; es decir, COM+ hace referencia a la información de catálogo del componente para proporcionar los servicios configurados. Sin embargo, puede optar por activar un componente configurado en el contexto predeterminado. Un componente COM base (un componente registrado que no tiene información de catálogo de COM+) se activa normalmente en el contexto predeterminado.

La activación de un componente COM en el contexto predeterminado proporciona tres ventajas de rendimiento principales, como se indica a continuación:

-   Los recursos del sistema se guardan limitando el número de contextos que se crean.
-   Para aumentar el rendimiento, limite el número de llamadas entre contextos. Dado que las llamadas entre contextos requieren serialización, es mucho más rápido que un objeto COM activado en el contexto predeterminado realice llamadas a otros objetos en el contexto predeterminado. El rendimiento en este caso (de llamadas dentro del mismo contexto) es similar al de llamar a una subrutina.
-   Puede importar aplicaciones COM antiguas en COM+ y ejecutarlas sin problemas. Por ejemplo, puede tener varias aplicaciones COM anteriores implementadas bajo la suposición de que se permite pasar referencias de objeto dentro de un apartamento sin calcular las referencias de las referencias. Estas aplicaciones COM no funcionan cuando se importan en COM+ porque las referencias de objeto se pasan a través de los límites del contexto. Sin embargo, puede hacer que este tipo de aplicación COM se ejecute cuando se importe si usa la herramienta administrativa Servicios de componentes para marcar todas las clases de la aplicación como **se debe activar en el contexto predeterminado**.

La principal desventaja de activar un componente configurado en el contexto predeterminado es que COM+ no proporciona ninguno de los servicios configurados del componente. Hay un equilibrio entre el rendimiento mejorado y la capacidad de usar los servicios COM+.

Por ejemplo, supongamos que un componente COM no requiere ningún servicio COM+ (como [transacciones](com--transactions.md), [activación Just-in-Time](com--just-in-time-activation.md), [eventos](com--events.md), [componentes en cola](com--queued-components.md), [sincronización](com--synchronization.md)o [agrupación de objetos](com--object-pooling.md)) y que el componente realiza varias llamadas a otros componentes com que se pueden activar en el contexto predeterminado. En este caso, sería una buena idea activar el componente de llamada en el contexto predeterminado.

Si el componente COM requiere servicios COM+, no se puede marcar como **se debe activar en el contexto predeterminado**. Además, no hay ninguna ganancia de rendimiento real si un objeto COM activado en el contexto predeterminado realiza varias llamadas a objetos en otros contextos. (Para obtener más información, vea [contextos](com--contexts.md)).

**Para aplicar la activación en el contexto predeterminado**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente (ubicado en la carpeta **componentes** de cualquier aplicación com+ seleccionada) que desee activar en el contexto predeterminado y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .

3.  Active la casilla **debe activarse en el contexto predeterminado**.

4.  Haga clic en **OK**.

> [!Note]  
> Al ejecutar un componente configurado en el contexto predeterminado, COM+ no activa ninguno de los servicios configurados para ese componente. Estos servicios están disponibles de nuevo cuando se desactiva la casilla **se debe activar en el contexto predeterminado** y, posteriormente, se ejecuta el componente configurado en su propio contexto.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-in-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Forzar la activación en el contexto del autor de la llamada](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



