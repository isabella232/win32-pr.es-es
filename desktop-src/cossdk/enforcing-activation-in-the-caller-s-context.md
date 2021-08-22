---
description: Aplicación de la activación en el contexto de llamadores
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Aplicación de la activación en el contexto de llamadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42cb657ad7d11f61de0737ca7ac935d1d570649c3e0da9db9b63c79edea38cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567425"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Aplicación de la activación en el contexto del autor de la llamada

Puede controlar si un objeto se activa en su propio contexto. Cuando se usa la herramienta administrativa Servicios de componentes para requerir la activación de componentes en el contexto del autor de la llamada, ocurre lo siguiente cuando COM+ activa una instancia del componente en un contexto:

-   Si es posible, el objeto se activa en el contexto del creador.
-   Se produce un error en la activación de objetos si requiere su propio contexto; Se \_ devuelve CO E ATTEMPT TO CREATE OUTSIDE CLIENT \_ \_ \_ \_ \_ \_ CONTEXT.

Si el objeto requiere o no su propio contexto depende de su configuración en relación con el estado actual de las propiedades de contexto del autor de la llamada. Para obtener más información, [vea CONTEXTOS DE COM+.](com--contexts.md)

Le gustaría controlar la activación en ese nivel si algún aspecto del objeto no funcionaría correctamente si tiene su propio contexto. Por ejemplo, si el componente no admite la serialización y tiene su propio contexto, se producirá un error en las llamadas a él porque se interceptan las llamadas entre contextos y se realiza una serialización ligera.

**Para aplicar la activación en el contexto del autor de la llamada**

1.  En el panel de detalles de la herramienta administrativa Servicios  de componentes, haga clic con el botón derecho en el componente (ubicado en la carpeta Componentes de cualquier aplicación COM+ seleccionada) para el que va a establecer las propiedades de activación y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo propiedades del componente, haga clic en **la pestaña** Activación .

3.  Active la **casilla Must be activated in the callers context** (Debe activarse en el contexto de los llamadores).

4.  Haga clic en **Aceptar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-In-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aplicación de la activación en el contexto predeterminado](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



