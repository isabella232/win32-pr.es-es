---
description: La clase CTransformFilter es una clase base para implementar filtros de transformación.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: Clase CTransformFilter (Transfrm. h)
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
ms.openlocfilehash: d24c305b28641fcee366b4e906b87008decac014
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660376"
---
# <a name="ctransformfilter-class"></a>Clase CTransformFilter

![jerarquía de clases ctransformfilter](images/tfrm03.png)

La `CTransformFilter` clase es una clase base para implementar filtros de transformación. Esta clase está diseñada para implementar un filtro de transformación con un PIN de entrada y un PIN de salida. Usa asignadores independientes para el PIN de entrada y el de salida. Para crear un filtro que procese los datos en su lugar, use la clase [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Este filtro usa la clase [**CTransformInputPin**](ctransforminputpin.md) para su PIN de entrada y la clase [**CTransformOutputPin**](ctransformoutputpin.md) para su PIN de salida. Normalmente, no es necesario invalidar estas clases de PIN. La mayoría de los métodos de PIN llaman a los métodos correspondientes en la `CTransformFilter` clase, por lo que puede invalidar los métodos de filtro si es necesario. El filtro crea ambos PIN en el método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) . Si invalida las clases de PIN, debe invalidar **GetPin** para crear los pin personalizados.

Para usar esta clase, derive una nueva clase de `CTransformFilter` e implemente los métodos siguientes:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter:: transform**](ctransformfilter-transform.md)

Es posible que tenga que reemplazar también otros métodos, en función de los requisitos del filtro.

## <a name="media-types"></a>Tipos de medios

El PIN de entrada de este filtro no propone ningún tipo de medio. se basa en el filtro de nivel superior para proponer los tipos de medios para la conexión. La razón de este diseño es que en la mayoría de los casos, el filtro de nivel superior puede proporcionar más información sobre el formato. Por ejemplo, con formatos de vídeo, el filtro de nivel superior conoce las dimensiones de vídeo y la velocidad de fotogramas, mientras que el filtro de transformación no tiene ninguna manera de determinar esta información. Si desea cambiar este comportamiento, invalide el método [**GetMediaType**](ctransformfilter-getmediatype.md) del PIN de entrada. Cuando el filtro de nivel superior propone un tipo de medio, el PIN de entrada llama al método [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro (virtual puro).

Hasta que se conecte el PIN de entrada, el PIN de salida rechazará todas las conexiones y no devolverá ningún tipo de medio preferido. Una vez conectado el PIN de entrada, el PIN de salida devuelve una lista de tipos preferidos llamando al método [**GetMediaType**](ctransformfilter-getmediatype.md) del filtro. Comprueba los tipos de salida de la conexión a través del método [**CheckTransform**](ctransformfilter-checktransform.md) del filtro. (Ambos métodos son virtuales puros). Normalmente, el tipo de entrada determinará en parte los tipos de salida aceptables.

Dependiendo del filtro, puede que desee registrar algunos de los tipos de medios admitidos del filtro, de modo que el objeto de [asignador de filtros](filter-mapper.md) pueda localizar el filtro. Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).

## <a name="streaming"></a>Streaming

Esta clase no pone en cola los datos de salida. Cada ejemplo de salida se entrega dentro del método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) . El método **Receive** llama al método [**Transform**](ctransformfilter-transform.md) del filtro (también virtual puro) para procesar los datos.

Para obtener más información sobre el uso de esta clase, vea [escribir filtros de transformación](writing-transform-filters.md).



| Variables de miembro protegidas                                                | Descripción                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ bEOSDelivered**](ctransformfilter-m-beosdelivered.md)              | Marca que indica si el filtro ha enviado una notificación de final de secuencia.                          |
| [**m \_ bSampleSkipped**](ctransformfilter-m-bsampleskipped.md)            | Marca que indica si se ha quitado la muestra más reciente.                                         |
| [**m \_ bQualityChanged**](ctransformfilter-m-bqualitychanged.md)          | Marca que indica si ha cambiado la calidad.                                                    |
| [**m \_ csFilter**](ctransformfilter-m-csfilter.md)                        | Sección crítica que protege el estado del filtro.                                                        |
| [**m \_ csReceive**](ctransformfilter-m-csreceive.md)                      | Sección crítica que protege el estado de streaming.                                                     |
| [**m \_ pInput**](ctransformfilter-m-pinput.md)                            | Puntero al pin de entrada.                                                                               |
| [**m \_ pOutput**](ctransformfilter-m-poutput.md)                          | Puntero al pin de salida.                                                                              |
| Métodos públicos                                                            | Descripción                                                                                             |
| [**CTransformFilter**](ctransformfilter-ctransformfilter.md)             | Método de constructor.                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | Método de destructor.                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | Recupera el número de clavijas del filtro. Virtualiza.                                                    |
| [**GetPin**](ctransformfilter-getpin.md)                                 | Recupera un código PIN. Virtualiza.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Transforma una muestra de entrada para generar un ejemplo de salida. Virtualiza.                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | Se le llama cuando el filtro cambia al estado de pausa. Virtualiza.                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | Se le llama cuando el filtro cambia al estado Stopped. Virtualiza.                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | Notifica al filtro que se ha solicitado un cambio de calidad. Virtualiza.                                        |
| [**SetMediaType**](ctransformfilter-setmediatype.md)                     | Se le llama cuando el tipo de medio se establece en uno de los PIN del filtro. Virtualiza.                                 |
| [**CheckConnect**](ctransformfilter-checkconnect.md)                     | Determina si una conexión de PIN es adecuada. Virtualiza.                                               |
| [**BreakConnect**](ctransformfilter-breakconnect.md)                     | Libera un código PIN de una conexión. Virtualiza.                                                              |
| [**CompleteConnect**](ctransformfilter-completeconnect.md)               | Completa una conexión de PIN. Virtualiza.                                                                    |
| [**Aparecen**](ctransformfilter-receive.md)                               | Recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. Virtualiza. |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | Recupera un nuevo ejemplo de salida y lo inicializa.                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | Notifica al filtro que no se esperan datos adicionales del PIN de entrada. Virtualiza.                    |
| [**BeginFlush**](ctransformfilter-beginflush.md)                         | Comienza una operación de vaciado. Virtualiza.                                                                      |
| [**EndFlush**](ctransformfilter-endflush.md)                             | Finaliza una operación de vaciado. Virtualiza.                                                                        |
| [**NewSegment**](ctransformfilter-newsegment.md)                         | Notifica al filtro que los ejemplos multimedia recibidos después de que esta llamada se agrupe como un segmento. Virtualiza.      |
| Métodos virtuales puros                                                      | Descripción                                                                                             |
| [**CheckInputType**](ctransformfilter-checkinputtype.md)                 | Comprueba si un tipo de medio especificado es aceptable para la entrada.                                          |
| [**CheckTransform**](ctransformfilter-checktransform.md)                 | Comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.                             |
| [**DecideBufferSize**](ctransformfilter-decidebuffersize.md)             | Establece los requisitos de búfer del PIN de salida.                                                              |
| [**GetMediaType**](ctransformfilter-getmediatype.md)                     | Recupera un tipo de medio preferido para el PIN de salida.                                                    |
| Métodos IMediaFilter                                                      | Descripción                                                                                             |
| [**Stop**](ctransformfilter-stop.md)                                     | Detiene el filtro.                                                                                       |
| [**Pausar**](ctransformfilter-pause.md)                                   | Pausa el filtro.                                                                                      |
| Métodos IBaseFilter                                                       | Descripción                                                                                             |
| [**FindPin**](ctransformfilter-findpin.md)                               | Recupera el pin con el identificador especificado.                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




