---
description: Entrega de ejemplos
ms.assetid: 31aabb6d-dec6-41fa-b24d-35a77b67bc4a
title: Entrega de ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979b08a2aec8f33794f0f06ec80b6de10d9e270c40186c1e30e665bcee5ce7b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928565"
---
# <a name="delivering-samples"></a>Entrega de ejemplos

En este artículo se describe cómo un filtro entrega un ejemplo. Describe tanto el modelo de inserción, mediante [**métodos IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) como el modelo de extracción, mediante [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).

**Modelo de inserción: entrega de un ejemplo**

El pin de salida entrega un ejemplo llamando al método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o al método [**IMemInputPin::ReceiveMultiple,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) que es equivalente, pero entrega una matriz de ejemplos. El pin de entrada puede **bloquearse dentro de Receive** (o **ReceiveMultiple).** Si el pin puede bloquearse, su [**método IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) debe devolver S \_ OK. Si el pin garantiza que nunca se bloquee, **ReceiveCanBlock** debe devolver S \_ FALSE. El valor \_ devuelto S OK no significa que **Receive** siempre se bloquee, solo que podría.

Aunque **Receive** puede bloquear para esperar a que un recurso esté disponible, no debe bloquearse para esperar más datos del filtro ascendente. Si lo hace, puede producirse un interbloqueo en el que el filtro ascendente espera a que el filtro de nivel inferior libere el ejemplo, lo que nunca ocurre porque el filtro de nivel inferior está esperando en el filtro ascendente. Sin embargo, si un filtro tiene varios pines de entrada, un pin puede esperar a que otro pin reciba datos. Por ejemplo, el [filtro Mux avi](avi-mux-filter.md) hace esto para poder intercalar datos de audio y vídeo.

Un pin puede rechazar una muestra por varios motivos:

-   El pin se vacíe (vea [Flushing](flushing.md)).
-   El pin no está conectado.
-   El filtro se detiene.
-   Se produjo otro error.

El **método Receive** debe devolver S FALSE en el primer caso y un código de error en los demás \_ casos. El filtro ascendente debe dejar de enviar muestras cuando el código de retorno sea distinto de S \_ OK.

Puede considerar que los tres primeros casos son errores "esperados", en el sentido de que el filtro estaba en un estado incorrecto para recibir muestras. Un error inesperado sería uno que hace que el pin rechace una muestra aunque el pin esté en estado de recepción. Si se produce un error de este tipo, el pin debe enviar una notificación de fin de flujo de bajada y enviar un evento [**\_ EC ERRORABORT**](ec-errorabort.md) al administrador de filtros Graph.

En las DirectShow base, el método [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) comprueba los casos de error generales: vaciado, detenido, etc. La clase derivada deberá comprobar si hay errores específicos del filtro. En caso de error, el método [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) envía la notificación de fin de flujo y el evento \_ EC ERRORABORT.

**Modelo de extracción: solicitud de un ejemplo**

En la **interfaz IAsyncReader,** el pin de entrada solicita ejemplos del pin de salida mediante una llamada a uno de los métodos siguientes:

-   [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)

El **método Request** es asincrónico; el pin de entrada llama [**a IAsyncReader::WaitForNext para**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-waitfornext) esperar a que se complete la solicitud. Los otros dos métodos son sincrónicos.

**Cuándo entregar datos**

Un filtro siempre entrega ejemplos mientras se encuentra en estado en ejecución. En la mayoría de los casos, un filtro también entrega muestras mientras está en pausa. Esto permite que el gráfico apunte los datos para que la reproducción se inicie inmediatamente cuando se llame a **Ejecutar** (vea [Estados de filtro](filter-states.md)). Si el filtro no entrega datos mientras está en pausa, el método **IMediaFilter::GetState** del filtro debe devolver VFW S CANT CUE en estado \_ \_ \_ pausado. Este código de retorno indica al gráfico de filtro que no espere los datos del filtro antes de completar la transición de pausa. De lo contrario, **el método Pause** se bloqueará indefinidamente. Para obtener código de ejemplo, [**vea CBaseFilter::GetState**](cbasefilter-getstate.md).

Estos son algunos ejemplos de cuándo es posible que un filtro necesite devolver VFW \_ S \_ CANT \_ CUE:

-   Los orígenes activos, como los filtros de captura, no deben enviar datos mientras están en pausa. Vea [Generar datos en un filtro de captura.](producing-data-in-a-capture-filter.md)
-   Un filtro divisor podría o no enviar datos mientras está en pausa, dependiendo de la implementación. Si el filtro usa subprocesos independientes para poner en cola datos en cada pin de salida, puede enviar datos mientras está en pausa. Pero si el filtro usa un único subproceso para cada pin de salida, el primer pin podría bloquear el subproceso cuando llama a **Receive**, lo que impedirá que los demás pins envíen datos. En ese caso, debe devolver VFW \_ S \_ CANT \_ CUE.
-   Un filtro podría entregar datos esporádicamente. Por ejemplo, podría analizar un flujo de datos personalizado y filtrar algunos paquetes mientras se entregan otros. En ese caso, es posible que no se garantice que el filtro entregue datos mientras está en pausa.

Un filtro de origen (mediante el modelo de inserción) o un filtro de analizador (mediante el modelo de inserción/extracción) crea uno o varios subprocesos de streaming, que entregan ejemplos lo antes posible. Los filtros de nivel inferior, como descodificadores y transformaciones, normalmente envían datos solo cuando se llama a **Receive** en sus pines de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recepción y entrega de ejemplos](receiving-and-delivering-samples.md)
</dt> </dl>

 

 



