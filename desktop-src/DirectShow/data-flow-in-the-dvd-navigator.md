---
description: Data Flow en el navegador de DVD
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Data Flow en el navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a981d2d7b528163abb53478e9e8f2ab88d46c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362455"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Data Flow en el navegador de DVD

DVD Navigator tiene métodos para detener y pausar la reproducción. Estos métodos son similares , pero no idénticos, a **los métodos Stop** y **Pause** de [**IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol) Esta es la diferencia entre ellos:

-   Los **métodos IDvdControl2** cambian lo que el navegador de DVD lee del disco. No cambian el estado del gráfico.
-   Los **métodos IMediaControl** cambian el estado del gráfico. No cambian lo que el navegador de DVD lee del disco. (Hay una excepción importante, que se explica en la sección siguiente, relacionada con el **método Stop).**

Por ejemplo, [**el método IDvdControl2::P ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) emite el comando "Pausar" del anexo J, pero no pausa el \_ gráfico de filtros. Por otro [**lado, el :P IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) pausa el gráfico, pero no emite ningún comando DE DVD.

En general, use los **métodos IMediaControl::P ause** y **Stop** en lugar de los métodos **IDvdControl2 correspondientes.** Los **métodos IMediaControl** tienen latencias muy pequeñas, mientras que los métodos **IDvdControl2** pueden tener hasta dos segundos de latencia.

Detención de la reproducción

El comportamiento de [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) depende de una marca que se puede establecer con el [**método IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

-   Si la marca RESETOnStop de DVD es \_ **FALSE,** **IMediaControl::Stop** detiene el gráfico, pero no cambia el dominio del navegador de DVD. Cuando se llama a run de nuevo, la reproducción se reanuda desde la posición actual.
-   Si DVD \_ ResetOnStop es **TRUE,** **IMediaControl::Stop** hace que se restablezca el navegador de DVD. Cuando se llama a [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) de nuevo, el navegador de DVD se reproduce desde el dominio First Play, como si estuviera insertando el DVD por primera vez.

La marca \_ RESETOnStop de DVD es **TRUE** de forma predeterminada, por compatibilidad con aplicaciones anteriores. Sin embargo, por lo general, debe invalidar el valor predeterminado y establecer la marca en **FALSE.** El motivo es que determinados eventos pueden hacer que el gráfico se detenga durante la reproducción. Por ejemplo, si cambia la resolución de pantalla, el gráfico de filtros se detiene, vuelve a conectar el representador de vídeo y se reinicia. Si DVD \_ ResetOnStop es **TRUE,** la reproducción se reiniciará desde el principio del disco. Probablemente no es lo que espera el usuario.

Por lo tanto, al principio de la aplicación, llame a **SetOption** con DVD \_ ResetOnStop establecido en **FALSE.** Si desea detener la reproducción y hacer que se reanude desde la misma ubicación, llame a **IMediaControl::Stop** o **IMediaControl::P ause**. Si desea detener la reproducción y restablecer el disco, llame a **SetOption** con DVD ResetOnStop igual a TRUE; a continuación, llame a \_ **IMediaControl::Stop;** por último, vuelva a llamar a **SetOption** y restablezca DVD \_ ResetOnStop en **FALSE.**

Pausar la reproducción

Si le da un comando al navegador de DVD mientras el gráfico está en pausa, es posible que el comando no se complete hasta que el gráfico se vuelva a ejecutar. En algunas situaciones, esto puede provocar un interbloqueo en la aplicación. Hay dos reglas que debe seguir para evitar interbloqueos:

-   Mientras esté en pausa, no emita más de un comando de DVD asincrónico.
-   Mientras esté en pausa, no bloquee el subproceso de interfaz de usuario de la aplicación ni el subproceso que cambia el estado del gráfico.

La segunda regla merece la pena examinarla con más detalle. Estos son algunos escenarios específicos que pueden provocar un interbloqueo:

-   **Escenario:** mientras está en pausa, la aplicación emite un comando DE DVD con la marca de bloqueo. Esto puede provocar un interbloqueo si el subproceso que emite el comando DVD es el mismo subproceso que emite el comando de ejecución. El comando DVD se bloquea hasta que se ejecuta el gráfico, pero el gráfico no se puede ejecutar hasta que se complete el comando.

    **Recomendación:** emita el comando DVD en un subproceso de trabajo independiente o no use la marca de bloqueo.

-   **Escenario:** mientras está en pausa, la aplicación emite un comando DVD y, a continuación, llama a [**IDvdCmd::WaitForEnd en**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) el objeto de comando. Esta situación es equivalente al ejemplo anterior. Si llama a **Wait** desde el subproceso de la interfaz de usuario, el subproceso de interfaz de usuario no puede ejecutar el gráfico hasta que el método **Wait** se desbloquee, pero el método **Wait** no se desbloqueará hasta que se ejecute el gráfico.

    **Recomendación:** Llame **a Wait** en un subproceso de trabajo.

-   **Escenario:** mientras se ejecuta el gráfico, la aplicación emite un comando DVD con la marca de bloqueo y, a continuación, llama a pause desde otro subproceso. Se trata de una posible condición de carrera porque el gráfico puede pausar antes de que se emita el comando. Si uno de los dos subprocesos es el subproceso de interfaz de usuario, puede producir un interbloqueo similar al de los dos ejemplos anteriores. En este ejemplo se muestra la importancia de escribir código seguro para subprocesos si la aplicación usa varios subprocesos.

    **Recomendación:** si usa subprocesos de trabajo, asegúrese de que el código es seguro para subprocesos.

-   **Escenario:** mientras está en pausa, la aplicación deshabilita el comando run desde la interfaz de usuario y, a continuación, emite un comando de DVD asincrónico. Este caso no es estrictamente un interbloqueo, porque el subproceso de aplicación todavía se está ejecutando. Sin embargo, ahora se impide que el usuario ejecute el gráfico y, por tanto, el comando nunca se completará.

    **Recomendación:** al pausar, deje siempre habilitado el comando de ejecución.

Buscar un DVD a una hora especificada

Para buscar con precisión una hora especificada en un disco, llame a [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). A continuación, llame [**a IDvdControl2::P layAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), especificando la hora y estableciendo *dwFlags* en DVD \_ CMD FLAG \_ \_ Flush.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



