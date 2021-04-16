---
description: Forzar la activación en el contexto de llamadores
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Forzar la activación en el contexto de llamadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686432"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Forzar la activación en el contexto del autor de la llamada

Puede controlar si un objeto se activa en su propio contexto. Cuando se usa la herramienta administrativa Servicios de componentes para requerir la activación del componente en el contexto del autor de la llamada, ocurre lo siguiente cuando COM+ activa una instancia del componente en un contexto:

-   Si es posible, el objeto se activa en el contexto del creador.
-   Se produce un error en la activación del objeto si necesita su propio contexto; \_ \_ \_ Se devuelve el intento de \_ crear un contexto de \_ \_ cliente externo \_ .

El hecho de que el objeto requiera o no su propio contexto depende de su configuración en relación con el estado actual de las propiedades de contexto del llamador. Para obtener más información, vea [contextos de com+](com--contexts.md).

Querrá controlar la activación en ese nivel de precisión si algún aspecto del objeto no funcionaría correctamente si tiene su propio contexto. Por ejemplo, si el componente no admite el cálculo de referencias y tiene su propio contexto, se producirá un error en cualquier llamada a él porque se interceptan las llamadas entre contextos y se realiza una serialización ligera.

**Para aplicar la activación en el contexto del autor de la llamada**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente (ubicado en la carpeta **componentes** de cualquier aplicación com+ seleccionada) para el que está configurando las propiedades de activación y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .

3.  Active la casilla **debe activarse en el contexto de llamadores** .

4.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-in-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Forzar la activación en el contexto predeterminado](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



