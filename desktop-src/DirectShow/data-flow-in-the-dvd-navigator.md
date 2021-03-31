---
description: Flujo de datos en el navegador de DVD
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Flujo de datos en el navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a981d2d7b528163abb53478e9e8f2ab88d46c0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806721"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Flujo de datos en el navegador de DVD

El navegador de DVD tiene métodos para detener y pausar la reproducción. Estos métodos son similares, pero no idénticos, a los métodos **Stop** y **PAUSE** en [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Esta es la diferencia entre ellos:

-   Los métodos de **IDvdControl2** cambian lo que el navegador de DVD Lee del disco. No cambian el estado del gráfico.
-   Los métodos **IMediaControl** cambian el estado del gráfico. No cambian lo que el navegador de DVD Lee del disco. (Hay una excepción importante, que se explica en la siguiente sección, relacionada con el método **Stop** ).

Por ejemplo, [**IDvdControl2::P método ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) emite el comando "PAUSE on" del Anexo J \_ , pero no pausa el gráfico de filtro. El método [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) , por otro lado, pone en pausa el gráfico pero no emite ningún comando de DVD.

En general, use los métodos **IMediaControl::P ause** y **Stop** en lugar de los métodos **IDvdControl2** correspondientes. Los métodos **IMediaControl** tienen latencias muy pequeñas, mientras que los métodos **IDvdControl2** pueden tener hasta dos segundos de latencia.

Detener la reproducción

El comportamiento de [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) depende de una marca que se puede establecer con el método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

-   Si la \_ marca ResetOnStop de DVD es **falsa**, **IMediaControl:: Stop** detiene el gráfico, pero no cambia el dominio del explorador de DVD. Cuando vuelva a llamar a ejecutar, la reproducción se reanudará desde la posición actual.
-   Si DVD \_ ResetOnStop es **true**, **IMediaControl:: Stop** hace que se restablezca el navegador de DVD. Cuando se llama de nuevo a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , el explorador de DVD se reproduce desde el primer dominio de reproducción, como si estuviera insertando el DVD por primera vez.

La \_ marca ResetOnStop de DVD es **true** de forma predeterminada, por compatibilidad con aplicaciones anteriores. Sin embargo, por lo general, debe reemplazar el valor predeterminado y establecer la marca en **false**. La razón es que ciertos eventos pueden hacer que el gráfico se detenga durante la reproducción. Por ejemplo, si la resolución de pantalla cambia, el gráfico de filtro se detiene, vuelve a conectar el representador de vídeo y se reinicia. Si DVD \_ ResetOnStop es **true**, la reproducción se reiniciará desde el principio del disco. Probablemente no sea lo que el usuario espera.

Al principio de la aplicación, por lo tanto, llame a **SetOption** con el DVD \_ ResetOnStop establecido en **false**. Si desea detener la reproducción y reanudarla desde la misma ubicación, llame a **IMediaControl:: Stop** o a **IMediaControl::P ause**. Si desea detener la reproducción y restablecer el disco, llame a **SetOption** con el DVD \_ ResetOnStop igual a **true**; a continuación, llame a **IMediaControl:: Stop**; por último, vuelva a llamar a **SetOption** y restablezca el \_ ResetOnStop de DVD en **false**.

Pausar la reproducción

Si asigna un comando al navegador de DVD mientras el gráfico está en pausa, es posible que el comando no se complete hasta que el gráfico vuelva a ejecutarse. En algunas situaciones, esto puede provocar un interbloqueo en la aplicación. Hay dos reglas que debe seguir para evitar los interbloqueos:

-   Mientras está en pausa, no emita más de un comando de DVD asincrónico.
-   Mientras está en pausa, no bloquee el subproceso de interfaz de usuario de la aplicación o el subproceso que cambia el estado del gráfico.

Merece la pena examinar la segunda regla con más detalle. Estos son algunos escenarios específicos que pueden provocar un interbloqueo:

-   **Escenario**: mientras se pausa, la aplicación emite un comando de DVD con la marca de bloqueo. Esto puede producir un interbloqueo si el subproceso que emite el comando de DVD es el mismo subproceso que emite el comando de ejecución. El comando de DVD se bloquea hasta que se ejecuta el gráfico, pero el gráfico no se puede ejecutar hasta que se complete el comando.

    **Recomendación**: emita el comando de DVD en un subproceso de trabajo independiente o no use la marca de bloqueo.

-   **Escenario**: mientras se pausa, la aplicación emite un comando de DVD y, a continuación, llama a [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) en el objeto de comando. Esta situación es equivalente al ejemplo anterior. Si llama a **Wait** desde el subproceso de la interfaz de usuario, el subproceso de interfaz de usuario no puede ejecutar el gráfico hasta que el método **Wait** se desbloquee, pero el método **Wait** no se desbloqueará hasta que se ejecute el gráfico.

    **Recomendación**: llame a **Wait** en un subproceso de trabajo.

-   **Escenario**: mientras el grafo se está ejecutando, la aplicación emite un comando de DVD con la marca de bloqueo y, a continuación, llama a PAUSE desde otro subproceso. Se trata de una posible condición de carrera porque el gráfico puede pausarse antes de que se emita el comando. Si uno de los dos subprocesos es el subproceso de la interfaz de usuario, puede producirse un interbloqueo similar a los dos ejemplos anteriores. En este ejemplo se muestra la importancia de escribir código seguro para subprocesos si la aplicación usa varios subprocesos.

    **Recomendación**: Si usa subprocesos de trabajo, asegúrese de que el código es seguro para subprocesos.

-   **Escenario**: mientras está en pausa, la aplicación deshabilita el comando ejecutar desde la interfaz de usuario y, después, emite un comando de DVD asincrónico. Este caso no es estrictamente un interbloqueo, porque el subproceso de la aplicación todavía se está ejecutando. Sin embargo, el usuario ahora no podrá ejecutar el gráfico y, por lo tanto, el comando nunca se completará.

    **Recomendación**: al pausar, deje siempre el comando ejecutar habilitado.

Búsqueda de un DVD en un período de tiempo especificado

Para buscar con precisión una hora especificada en un disco, llame a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). A continuación, llame a [**IDvdControl2::P layattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), especificando la hora y el valor de *dwFlags* en el \_ \_ vaciado de la marca de CMD \_ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



