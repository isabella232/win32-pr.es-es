---
description: Entrega de ejemplos
ms.assetid: 31aabb6d-dec6-41fa-b24d-35a77b67bc4a
title: Entrega de ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083bc8c88649c04bdf9f93f86ebcc277ee48e75e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423164"
---
# <a name="delivering-samples"></a>Entrega de ejemplos

En este artículo se describe cómo un filtro proporciona un ejemplo. Describe el modelo de inserción, el uso de métodos [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) y el modelo de extracción mediante [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).

**Modelo de envío: entrega de un ejemplo**

El PIN de salida proporciona una muestra llamando al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o al método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) , que es equivalente pero proporciona una matriz de ejemplos. El PIN de entrada puede bloquearse dentro de la **recepción** (o **ReceiveMultiple**). Si el PIN podría bloquearse, su método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) debe devolver S \_ correcto. Si el PIN no garantiza nunca el bloqueo, **ReceiveCanBlock** debe devolver S \_ false. El \_ valor devuelto de S correcto no significa que **reciba** siempre bloques, solo que podría.

Aunque **Receive** puede bloquearse para esperar a que un recurso esté disponible, no debe bloquearse para esperar más datos del filtro de nivel superior. Si lo hace, puede producirse un interbloqueo en el que el filtro ascendente espera a que el filtro de nivel inferior libere el ejemplo, lo que nunca sucede porque el filtro de nivel inferior está esperando en el filtro de nivel superior. Sin embargo, si un filtro tiene varios PIN de entrada, un pin puede esperar a que otro PIN reciba datos. Por ejemplo, el filtro de [AVI MUX](avi-mux-filter.md) hace esto para que pueda intercalar datos de audio y vídeo.

Un PIN podría rechazar un ejemplo por una serie de motivos:

-   El PIN se está vaciando (vea el [vaciado](flushing.md)).
-   El PIN no está conectado.
-   El filtro está detenido.
-   Se produjo algún otro error.

El método **Receive** debe devolver S \_ false en el primer caso y un código de error en los demás casos. El filtro de nivel superior debe dejar de enviar ejemplos cuando el código de retorno es distinto de S \_ correcto.

Puede considerar que los tres primeros casos son errores "esperados", en el sentido de que el filtro se encontraba en un estado incorrecto para recibir ejemplos. Un error inesperado sería el que provocaría que el PIN rechazara un ejemplo aunque el PIN esté en un estado de recepción. Si se produce un error de este tipo, el PIN debe enviar una notificación de final de secuencia de nivel inferior y enviar un evento [**\_ ERRORABORT de EC**](ec-errorabort.md) al administrador de gráficos de filtro.

En las clases base de DirectShow, el método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) comprueba los casos de error generales: vaciado, detenido, etc. La clase derivada deberá comprobar si hay errores que sean específicos del filtro. En caso de error, el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) envía la notificación de final de secuencia y el \_ evento ERRORABORT de EC.

**Modelo de extracción: solicitar un ejemplo**

En la interfaz **IAsyncReader** , el PIN de entrada solicita ejemplos del PIN de salida llamando a uno de los métodos siguientes:

-   [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)

El método de **solicitud** es asincrónico; el PIN de entrada llama a [**IAsyncReader:: WaitForNext**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-waitfornext) para esperar a que se complete la solicitud. Los otros dos métodos son sincrónicos.

**Cuándo enviar datos**

Un filtro siempre entrega los ejemplos mientras se encuentra en el estado en ejecución. En la mayoría de los casos, un filtro también proporciona ejemplos mientras están en pausa. Esto permite que el gráfico señale los datos para que la reproducción se inicie inmediatamente cuando se llame a **Run** (consulte [Estados de filtro](filter-states.md)). Si el filtro no entrega datos mientras está en pausa, el método **IMediaFilter:: GetState** del filtro debe devolver \_ la indicación VFW s \_ peralte \_ en el estado pausado. Este código de retorno indica al gráfico de filtro que no espere los datos del filtro antes de completar la transición de pausa. De lo contrario, el método **PAUSE** se bloqueará indefinidamente. Para obtener código de ejemplo, vea [**CBaseFilter:: GetState**](cbasefilter-getstate.md).

Estos son algunos ejemplos de Cuándo puede ser necesario que un filtro devuelva la indicación de no \_ \_ peralte de VFW \_ :

-   Los orígenes en directo, como los filtros de captura, no deben enviar datos mientras están en pausa. Vea [generar datos en un filtro de captura](producing-data-in-a-capture-filter.md).
-   Un filtro divisor podría o no enviar datos mientras están en pausa, dependiendo de la implementación. Si el filtro usa subprocesos independientes para poner en cola los datos en cada terminal de salida, puede enviar datos mientras están en pausa. Pero si el filtro usa un solo subproceso para cada pin de salida, el primer PIN podría bloquear el subproceso cuando llame a **Receive**, lo que impedirá que los demás PIN envíen datos. En ese caso, debe devolver la \_ indicación VFW S \_ peralte \_ .
-   Un filtro podría proporcionar datos esporádicamente. Por ejemplo, puede analizar un flujo de datos personalizado y filtrar algunos paquetes mientras entrega otros. En ese caso, es posible que no se garantice que el filtro entregue datos mientras esté en pausa.

Un filtro de origen (con el modelo de inserción) o un filtro de analizador (mediante el modelo de inserción/extracción) crea uno o más subprocesos de streaming, que proporcionan ejemplos lo más rápido posible. Los filtros de nivel inferior, como descodificadores y transformaciones, normalmente envían datos solo cuando se llama a **Receive** en sus clavijas de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recibir y entregar ejemplos](receiving-and-delivering-samples.md)
</dt> </dl>

 

 



