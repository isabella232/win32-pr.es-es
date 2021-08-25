---
description: La clase CTransformFilter es una clase base para implementar filtros de transformación.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: CTransformFilter (clase, Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9d199a406fa1934fb63625cd258baee8d69c20c17992a7d1d3bbd2c83956a1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633904"
---
# <a name="ctransformfilter-class"></a>CTransformFilter (clase)

![Jerarquía de clases ctransformfilter](images/tfrm03.png)

La `CTransformFilter` clase es una clase base para implementar filtros de transformación. Esta clase está diseñada para implementar un filtro de transformación con un pin de entrada y un pin de salida. Usa asignadores independientes para el pin de entrada y el pin de salida. Para crear un filtro que procese los datos en su lugar, use la [**clase CTransInPlaceFilter.**](ctransinplacefilter.md)

Este filtro usa la [**clase CTransformInputPin**](ctransforminputpin.md) para su pin de entrada y la clase [**CTransformOutputPin**](ctransformoutputpin.md) para su pin de salida. Normalmente, no es necesario invalidar estas clases de pin. La mayoría de los métodos pin llaman a los métodos correspondientes en la clase , por lo `CTransformFilter` que puede invalidar los métodos de filtro si es necesario. El filtro crea ambos pines en el [**método CTransformFilter::GetPin.**](ctransformfilter-getpin.md) Si invalida las clases de pin, debe invalidar **GetPin** para crear los pines personalizados.

Para usar esta clase, derive una nueva clase de `CTransformFilter` e implemente los métodos siguientes:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter::Transform**](ctransformfilter-transform.md)

Es posible que también tenga que invalidar otros métodos, en función de los requisitos del filtro.

## <a name="media-types"></a>Tipos de medios

El pin de entrada de este filtro no propone ningún tipo de medio; se basa en el filtro ascendente para proponer los tipos de medios para la conexión. El motivo de este diseño es que, en la mayoría de los casos, el filtro ascendente puede proporcionar más información sobre el formato. Por ejemplo, con los formatos de vídeo, el filtro ascendente conoce las dimensiones de vídeo y la velocidad de fotogramas, mientras que el filtro de transformación no tiene forma de determinar esta información. Si desea cambiar este comportamiento, invalide el método [**GetMediaType**](ctransformfilter-getmediatype.md) del pin de entrada. Cuando el filtro ascendente propone un tipo de medio, el pin de entrada llama al [**método CheckInputType**](ctransformfilter-checkinputtype.md) del filtro (virtual puro).

Hasta que el pin de entrada está conectado, el pin de salida rechaza todas las conexiones y no devuelve ningún tipo de medio preferido. Una vez conectado el pin de entrada, el pin de salida devuelve una lista de tipos preferidos mediante una llamada al [**método GetMediaType del**](ctransformfilter-getmediatype.md) filtro. Comprueba los tipos de salida de la conexión a través del [**método CheckTransform del**](ctransformfilter-checktransform.md) filtro. (Ambos métodos son virtuales puros). Normalmente, el tipo de entrada determinará parcialmente los tipos de salida aceptables.

Según el filtro, es posible que desee registrar algunos de los tipos de medios admitidos del filtro, para que el objeto [Filter Mapper](filter-mapper.md) pueda localizar el filtro. Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="streaming"></a>Streaming

Esta clase no pone en cola los datos de salida. Cada ejemplo de salida se entrega dentro del [**método IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) El **método Receive** llama al método [**Transform**](ctransformfilter-transform.md) del filtro (también virtual puro) para procesar los datos.

Para obtener más información sobre el uso de esta clase, vea [Escribir filtros de transformación](writing-transform-filters.md).



| Variables de miembro protegido                                                | Descripción                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ bEOSDelivered**](ctransformfilter-m-beosdelivered.md)              | Marca que indica si el filtro ha enviado una notificación de fin de flujo.                          |
| [**m \_ bSampleSkipped**](ctransformfilter-m-bsampleskipped.md)            | Marca que indica si se ha eliminado la muestra más reciente.                                         |
| [**m \_ bQualityChanged**](ctransformfilter-m-bqualitychanged.md)          | Marca que indica si la calidad ha cambiado.                                                    |
| [**m \_ csFilter**](ctransformfilter-m-csfilter.md)                        | Sección crítica que protege el estado del filtro.                                                        |
| [**m \_ csReceive**](ctransformfilter-m-csreceive.md)                      | Sección crítica que protege el estado de streaming.                                                     |
| [**m \_ pInput**](ctransformfilter-m-pinput.md)                            | Puntero al pin de entrada.                                                                               |
| [**m \_ pOutput**](ctransformfilter-m-poutput.md)                          | Puntero al pin de salida.                                                                              |
| Métodos públicos                                                            | Descripción                                                                                             |
| [**CTransformFilter**](ctransformfilter-ctransformfilter.md)             | Método constructor.                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | Método destructor.                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | Recupera el número de pines del filtro. Virtual.                                                    |
| [**GetPin**](ctransformfilter-getpin.md)                                 | Recupera un pin. Virtual.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Transforma un ejemplo de entrada para generar un ejemplo de salida. Virtual.                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | Se llama cuando el filtro cambia al estado en pausa. Virtual.                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | Se llama cuando el filtro cambia al estado detenido. Virtual.                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | Notifica al filtro que se solicita un cambio de calidad. Virtual.                                        |
| [**SetMediaType**](ctransformfilter-setmediatype.md)                     | Se llama cuando el tipo de medio se establece en uno de los pines del filtro. Virtual.                                 |
| [**CheckConnect**](ctransformfilter-checkconnect.md)                     | Determina si una conexión de pin es adecuada. Virtual.                                               |
| [**BreakConnect**](ctransformfilter-breakconnect.md)                     | Libera un pin de una conexión. Virtual.                                                              |
| [**CompleteConnect**](ctransformfilter-completeconnect.md)               | Completa una conexión de pin. Virtual.                                                                    |
| [**Recibir**](ctransformfilter-receive.md)                               | Recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. Virtual. |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | Recupera un nuevo ejemplo de salida y lo inicializa.                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | Notifica al filtro que no se espera ningún dato adicional del pin de entrada. Virtual.                    |
| [**BeginFlush**](ctransformfilter-beginflush.md)                         | Comienza una operación de vaciado. Virtual.                                                                      |
| [**EndFlush**](ctransformfilter-endflush.md)                             | Finaliza una operación de vaciado. Virtual.                                                                        |
| [**NewSegment**](ctransformfilter-newsegment.md)                         | Notifica al filtro que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento. Virtual.      |
| Métodos virtuales puros                                                      | Descripción                                                                                             |
| [**CheckInputType**](ctransformfilter-checkinputtype.md)                 | Comprueba si un tipo de medio especificado es aceptable para la entrada.                                          |
| [**CheckTransform**](ctransformfilter-checktransform.md)                 | Comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.                             |
| [**DecideBufferSize**](ctransformfilter-decidebuffersize.md)             | Establece los requisitos de búfer del pin de salida.                                                              |
| [**GetMediaType**](ctransformfilter-getmediatype.md)                     | Recupera un tipo de medio preferido para la patilla de salida.                                                    |
| Métodos IMediaFilter                                                      | Descripción                                                                                             |
| [**Stop**](ctransformfilter-stop.md)                                     | Detiene el filtro.                                                                                       |
| [**Pausar**](ctransformfilter-pause.md)                                   | Pausa el filtro.                                                                                      |
| Métodos IBaseFilter                                                       | Descripción                                                                                             |
| [**FindPin**](ctransformfilter-findpin.md)                               | Recupera el pin con el identificador especificado.                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




