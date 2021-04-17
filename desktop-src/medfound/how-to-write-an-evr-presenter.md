---
description: En este artículo se describe cómo escribir un presentador personalizado para el representador de vídeo mejorado (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Cómo escribir un presentador de EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557251"
---
# <a name="how-to-write-an-evr-presenter"></a>Cómo escribir un presentador de EVR

En este artículo se describe cómo escribir un presentador personalizado para el representador de vídeo mejorado (EVR). Un presentador personalizado se puede usar con DirectShow y Media Foundation; las interfaces y el modelo de objetos son los mismos para ambas tecnologías, aunque la secuencia exacta de operaciones puede variar.

El código de ejemplo de este tema se adapta desde el [ejemplo EVRPresenter](evrpresenter-sample.md), que se proporciona en el Windows SDK.

Este tema contiene las siguientes secciones:

-   [Requisitos previos](#prerequisites)
-   [Modelo de objetos de moderador](#presenter-object-model)
    -   [Flujo de datos dentro de EVR](#data-flow-inside-the-evr)
    -   [Estados del presentador](#presenter-states)
    -   [Interfaces de moderador](#presenter-interfaces)
    -   [Implementación de IMFVideoDeviceID](#implementing-imfvideodeviceid)
    -   [Implementación de IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)
    -   [Implementación de IMFVideoPresenter](#implementing-imfvideopresenter)
    -   [Implementación de IMFClockStateSink](#implementing-imfclockstatesink)
    -   [Implementación de IMFRateSupport](#implementing-imfratesupport)
    -   [Envío de eventos a EVR](#sending-events-to-the-evr)
-   [Formatos de negociación](#negotiating-formats)
-   [Administrar el dispositivo Direct3D](#managing-the-direct3d-device)
    -   [Asignación de superficies de Direct3D](#allocating-direct3d-surfaces)
    -   [Ejemplos de seguimiento](#tracking-samples)
-   [Procesar la salida](#processing-output)
    -   [Volver a dibujar marcos](#repainting-frames)
    -   [Ejemplos de programación](#scheduling-samples)
    -   [Presentar ejemplos](#presenting-samples)
    -   [Rectángulos de origen y de destino](#source-and-destination-rectangles)
    -   [Final de la secuencia](#end-of-stream)
-   [Recorrido de fotogramas](#frame-stepping)
    -   [Implementación del recorrido de fotogramas](#implementing-frame-stepping)
-   [Establecer el presentador en el EVR](#setting-the-presenter-on-the-evr)
    -   [Establecer el presentador en DirectShow](#setting-the-presenter-in-directshow)
    -   [Establecer el presentador en Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Antes de escribir un presentador personalizado, debe estar familiarizado con las siguientes tecnologías:

-   El representador de vídeo mejorado. Consulte [representador de vídeo mejorado](enhanced-video-renderer.md).
-   Gráficos de Direct3D. No es necesario comprender los gráficos 3D para escribir un presentador, pero debe saber cómo crear un dispositivo Direct3D y administrar superficies de Direct3D. Si no está familiarizado con Direct3D, lea las secciones "dispositivos Direct3D" y "recursos de Direct3D" en la documentación del SDK de gráficos de DirectX.
-   Gráficos de filtros de DirectShow o la canalización de Media Foundation, en función de la tecnología que utilizará la aplicación para representar vídeo.
-   [Media Foundation transformaciones](media-foundation-transforms.md). EVR mixer es una transformación de Media Foundation y el presentador llama a los métodos directamente en el mezclador.
-   Implementar objetos COM. El presentador es un objeto COM en proceso y de subprocesamiento libre.

## <a name="presenter-object-model"></a>Modelo de objetos de moderador

Esta sección contiene información general sobre el modelo de objetos y las interfaces del presentador.

### <a name="data-flow-inside-the-evr"></a>Flujo de datos dentro de EVR

EVR usa dos componentes de complemento para representar vídeo: el *mezclador* y el *presentador*. El mezclador combina las secuencias de vídeo y desentrelaza el vídeo si es necesario. El presentador dibuja (o *presenta*) el vídeo en la pantalla y programa Cuándo se dibuja cada fotograma. Las aplicaciones pueden reemplazar cualquiera de estos objetos por una implementación personalizada.

EVR tiene uno o varios flujos de entrada y el mezclador tiene un número correspondiente de flujos de entrada. Stream 0 siempre es el *flujo de referencia*. Los demás flujos son *subflujos*, que el mezclador alfa combina en el flujo de referencia. La secuencia de referencia determina la velocidad de fotogramas principal del vídeo compuesto. En cada fotograma de referencia, el mezclador toma el fotograma más reciente de cada subflujo, lo combina alfa en el fotograma de referencia y genera un único fotograma compuesto. El mezclador también realiza desentrelazado y conversión de color de YUV a RGB si es necesario. EVR siempre inserta el mezclador en la canalización de vídeo, independientemente del número de flujos de entrada o el formato de vídeo. En la imagen siguiente se ilustra este proceso.

![diagrama que muestra la secuencia de referencia y el subflujo que apunta al mezclador, que señala al presentador, que apunta a la pantalla.](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

El presentador realiza las siguientes tareas:

-   Establece el formato de salida en el mezclador. Antes de que comience el streaming, el presentador establece un tipo de medio en el flujo de salida del mezclador. Este tipo de medio define el formato de la imagen compuesta.
-   Crea el dispositivo Direct3D.
-   Asigna superficies de Direct3D. El mezclador blits los fotogramas compuestos en estas superficies.
-   Obtiene el resultado del mezclador.
-   Programa Cuándo se presentan los fotogramas. EVR proporciona el reloj de la presentación y el presentador programa fotogramas según este reloj.
-   Presenta cada fotograma mediante Direct3D.
-   Realiza el recorrido y la limpieza de fotogramas.

### <a name="presenter-states"></a>Estados del presentador

En cualquier momento, el presentador se encuentra en uno de los siguientes Estados:

-   *Iniciado*. El reloj de la presentación de EVR se está ejecutando. El presentador programa fotogramas de vídeo para su presentación a medida que llegan.
-   En *pausa*. El reloj de la presentación se suspende. El presentador no presenta ningún ejemplo nuevo, sino que mantiene su cola de ejemplos programados. Si se reciben muestras nuevas, el presentador las agrega a la cola.
-   *Detenido*. El reloj de la presentación está detenido. El presentador descarta cualquier ejemplo programado.
-   *Apagar*. El presentador libera todos los recursos relacionados con el streaming, como las superficies de Direct3D. Este es el estado inicial del presentador y el estado final antes de que se destruya el presentador.

En el código de ejemplo de este tema, el estado del presentador se representa mediante una enumeración:


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Algunas operaciones no son válidas mientras el presentador se encuentra en estado de cierre. En el código de ejemplo se comprueba este estado llamando a un método auxiliar:


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a>Interfaces de moderador

Se requiere un presentador para implementar las interfaces siguientes:



| Interfaz                                                                | Descripción                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Notifica al presentador cuando el reloj de EVR cambia de estado. Consulte [implementación de IMFClockStateSink](#implementing-imfclockstatesink).                                   |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Proporciona una forma para que la aplicación y otros componentes de la canalización obtengan interfaces del presentador.                                                       |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permite al presentador obtener interfaces de EVR o del mezclador. Consulte [implementación de IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient). |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Garantiza que el presentador y el mezclador usan tecnologías compatibles. Consulte [implementación de IMFVideoDeviceID](#implementing-imfvideodeviceid).                          |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Procesa los mensajes de EVR. Consulte [implementación de IMFVideoPresenter](#implementing-imfvideopresenter).                                                             |



 

Las siguientes interfaces son opcionales:



| Interfaz                                                | Descripción                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Permite al presentador trabajar con medios protegidos. Implemente esta interfaz si el presentador es un componente de confianza diseñado para funcionar en la ruta de acceso a medios protegidos (PMP). |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Indica el intervalo de velocidades de reproducción que admite el presentador. Consulte [implementación de IMFRateSupport](#implementing-imfratesupport).                                         |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Asigna coordenadas del fotograma de vídeo de salida a las coordenadas del fotograma de vídeo de entrada.                                                                                       |
| [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Informa de la información de rendimiento. EVR usa esta información para la administración del control de calidad. Esta interfaz está documentada en el SDK de DirectShow.                        |



 

También puede proporcionar interfaces para que la aplicación se comunique con el presentador. El presentador estándar implementa la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para este propósito. Puede implementar esta interfaz o definir la suya propia. La aplicación obtiene las interfaces del presentador llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en EVR. Cuando se **MR_VIDEO_RENDER_SERVICE** el GUID de servicio, el EVR pasa la solicitud **GetService** al presentador.

### <a name="implementing-imfvideodeviceid"></a>Implementación de IMFVideoDeviceID

La interfaz [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un método, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), que devuelve un GUID de dispositivo. El GUID del dispositivo garantiza que el presentador y el mezclador usan tecnologías compatibles. Si los GUID del dispositivo no coinciden, el EVR no se puede inicializar.

El mezclador y el presentador estándar usan Direct3D 9, con el GUID de dispositivo igual a **IID_IDirect3DDevice9**. Si piensa usar el presentador personalizado con el mezclador estándar, el GUID del dispositivo del presentador debe estar **IID_IDirect3DDevice9**. Si reemplaza ambos componentes, podría definir un nuevo GUID de dispositivo. En el resto de este artículo, se supone que el presentador usa Direct3D 9. Esta es la implementación estándar de [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



El método debe tener éxito incluso cuando se cierre el presentador.

### <a name="implementing-imftopologyservicelookupclient"></a>Implementación de IMFTopologyServiceLookupClient

La interfaz [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) permite al presentador obtener punteros de interfaz de EVR y del mezclador como se indica a continuación:

1.  Cuando EVR inicializa el presentador, llama al método [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentador. El argumento es un puntero a la interfaz [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) de EVR.
2.  El presentador llama a [**IMFTopologyServiceLookup:: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) para obtener punteros de interfaz desde EVR o el mezclador.

El método [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) es similar al método [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Ambos métodos toman un GUID de servicio y un identificador de interfaz (IID) como entrada, pero **LookupService** devuelve una matriz de punteros de interfaz, mientras que **GetService** devuelve un solo puntero. En la práctica, sin embargo, siempre puede establecer el tamaño de la matriz en 1. El objeto consultado depende del GUID del servicio:

-   Si se **MR_VIDEO_RENDER_SERVICE** el GUID de servicio, se consulta el EVR.
-   Si se **MR_VIDEO_MIXER_SERVICE** el GUID de servicio, se consulta el mezclador.

En la implementación de [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), obtenga las siguientes interfaces de EVR:



| Interfaz EVR                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Proporciona una manera para que el presentador envíe mensajes a EVR. Esta interfaz se define en el SDK de DirectShow, por lo que los mensajes siguen el patrón para los eventos de DirectShow, no Media Foundation eventos.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**IMFClock**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Representa el reloj de EVR. El presentador usa esta interfaz para programar ejemplos de presentación. El EVR se puede ejecutar sin un reloj, por lo que es posible que esta interfaz no esté disponible. Si no es así, omita el código de error de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).<br/> El reloj también implementa la interfaz [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) . En la canalización de Media Foundation, el reloj implementa la interfaz [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) . No implementa esta interfaz en DirectShow.<br/> |



 

Obtenga las siguientes interfaces del mezclador:



| Mezclador (interfaz)                              | Descripción                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Permite al presentador comunicarse con el mezclador.       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Permite al presentador validar el GUID del dispositivo del mezclador. |



 

El código siguiente implementa el método [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Cuando los punteros de interfaz obtenidos de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ya no son válidos, el EVR llama a [**IMFTopologyServiceLookupClient:: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers). Dentro de este método, libere todos los punteros de interfaz y establezca el estado del presentador en Apagar:


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



EVR llama a [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) por diversos motivos, entre los que se incluyen:

-   Desconectar o volver a conectar los pin (DirectShow), o agregar o quitar receptores de secuencias (Media Foundation).
-   Cambiando el formato.
-   Establecer un nuevo reloj.
-   Cierre final de EVR.

Durante la vigencia del presentador, el EVR podría llamar varias veces a [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) y [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) .

### <a name="implementing-imfvideopresenter"></a>Implementación de IMFVideoPresenter

La interfaz [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) hereda [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) y agrega dos métodos:



| Método                                                               | Descripción                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Devuelve el tipo de medio de los fotogramas de vídeo compuestos. |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Indica al presentador que realice varias acciones.      |



 

El método [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) devuelve el tipo de medio del presentador. (Para obtener más información acerca de cómo establecer el tipo de medio, vea [negociar formatos](#negotiating-formats)). El tipo de medio se devuelve como un puntero de interfaz [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) . En el ejemplo siguiente se da por supuesto que el presentador almacena el tipo de medio como un puntero [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Para obtener la interfaz **IMFVideoMediaType** del tipo de archivo multimedia, llame a **QueryInterface**:


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



El método [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) es el mecanismo principal para que EVR se comunique con el presentador. Se definen los siguientes mensajes. En el resto de este tema se proporcionan los detalles de la implementación de cada mensaje.



| Message                                | Descripción                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | El tipo de medio de salida del mezclador no es válido. El presentador debe negociar un nuevo tipo de medio con el mezclador. Vea [negociar formatos](#negotiating-formats).                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | Se ha iniciado la transmisión por secuencias. Este mensaje no requiere ninguna acción concreta, pero se puede utilizar para asignar recursos.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | La transmisión por secuencias ha finalizado. Libere todos los recursos asignados en respuesta al mensaje de **MFVP_MESSAGE_BEGINSTREAMING** .                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | El mezclador ha recibido una nueva muestra de entrada y es posible que pueda generar un nuevo fotograma de salida. El presentador debe llamar a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador. Consulte [procesar la salida](#processing-output). |
| **MFVP_MESSAGE_ENDOFSTREAM**         | La presentación ha finalizado. Vea [final de la secuencia](#end-of-stream).                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | EVR está vaciando los datos en su canalización de representación. El presentador debe descartar los fotogramas de vídeo programados para la presentación.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Solicita al presentador que reenvíe N fotogramas. El presentador debe descartar los siguientes N-1 fotogramas y mostrar el marco N. Consulte [recorrido de fotogramas](#frame-stepping).                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Cancela la ejecución del fotograma.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Implementación de IMFClockStateSink

El presentador debe implementar la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) como parte de su implementación de [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), que hereda **IMFClockStateSink**. EVR usa esta interfaz para notificar al presentador cada vez que el reloj del EVR cambie de estado. Para obtener más información sobre los Estados de reloj, vea [reloj de presentación](presentation-clock.md).

Estas son algunas directrices para implementar los métodos en esta interfaz. Se producirá un error en todos los métodos si se cierra el presentador.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></td>
<td><ol>
<li>Establezca el estado del presentador en iniciado.</li>
<li>Si <em>llClockStartOffset</em> no se <strong>PRESENTATION_CURRENT_POSITION</strong>, vacíe la cola de ejemplos del presentador. (Esto equivale a recibir un mensaje <strong>MFVP_MESSAGE_FLUSH</strong> ).</li>
<li>Si aún está pendiente una solicitud de paso de marco anterior, procese la solicitud (consulte <a href="#frame-stepping">ejecución de fotogramas</a>). De lo contrario, intente procesar la salida del mezclador (consulte <a href="#processing-output">procesamiento de salida</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></td>
<td><ol>
<li>Establezca el estado del presentador en detenido.</li>
<li>Vacíe la cola de ejemplos del presentador.</li>
<li>Cancele cualquier operación pendiente de paso de marco.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></td>
<td>Establezca el estado del presentador en pausado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></td>
<td>Trate lo mismo que <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> pero no vacíe la cola de ejemplos.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></td>
<td><ol>
<li>Si la velocidad cambia de cero a un valor distinto de cero, cancele el recorrido de los fotogramas.</li>
<li>Almacenar la nueva velocidad de reloj. La velocidad de reloj afecta a la presentación de los ejemplos. Para obtener más información, vea <a href="#scheduling-samples">ejemplos de programación</a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>Implementación de IMFRateSupport

Para admitir velocidades de reproducción distintas de 1 × velocidad, el presentador debe implementar la interfaz [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) . Estas son algunas directrices para implementar los métodos en esta interfaz. Se debe producir un error en todos los métodos después de apagar el presentador. Para obtener más información sobre esta interfaz, vea [control de tasa](rate-control.md).



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Devuelve cero para indicar que no hay ninguna velocidad mínima de reproducción.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | En el caso de la reproducción no simplificada, la velocidad de reproducción no debe superar la frecuencia de actualización del monitor: frecuencia de actualización de *velocidad máxima*  =   (Hz)/ *velocidad de fotogramas de vídeo* (FPS). La velocidad de fotogramas de vídeo se especifica en el tipo de medio del presentador. <br/> Para la reproducción simplificada, la velocidad de reproducción es ilimitada; Devuelve el valor **FLT_MAX**. En la práctica, el origen y el descodificador serán los factores de limitación durante la reproducción simplificada. <br/> Para la reproducción inversa, devuelva el valor negativo de la velocidad máxima.<br/> |
| [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Devuelve **MF_E_UNSUPPORTED_RATE** si el valor absoluto de *flRate* supera la velocidad de reproducción máxima del presentador. Calcule la velocidad de reproducción máxima tal y como se describe en [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).                                                                                                                                                                                                                                                                                    |



 

En el ejemplo siguiente se muestra cómo implementar el método [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



En el ejemplo anterior se llama a un método auxiliar, GetMaxRate, para calcular la velocidad máxima de reproducción de avance:

En el ejemplo siguiente se muestra cómo implementar el método [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a>Envío de eventos a EVR

El presentador debe notificar a EVR de varios eventos. Para ello, usa la interfaz [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) de EVR, que se obtiene cuando EVR llama al método [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentador. (La interfaz **IMediaEventSink** es originalmente una interfaz de DirectShow, pero se usa tanto en el EVR de DirectShow como en el Media Foundation). En el código siguiente se muestra cómo enviar un evento a EVR:


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



En la tabla siguiente se enumeran los eventos que envía el presentador, junto con los parámetros de evento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Evento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>El presentador ha finalizado la representación de todos los marcos después del mensaje de MFVP_MESSAGE_ENDOFSTREAM.<br/>
<ul>
<li><em>Parám1</em>: HRESULT que indica el estado de la operación.</li>
<li><em>Parám2</em>: no se usa.</li>
</ul>
Para obtener más información, vea <a href="#end-of-stream">final de la secuencia</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>El dispositivo Direct3D ha cambiado.<br/>
<ul>
<li><em>Parám1</em>: no se utiliza.</li>
<li><em>Parám2</em>: no se usa.</li>
</ul>
Para obtener más información, vea <a href="#managing-the-direct3d-device">administrar el dispositivo Direct3D</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>Se ha producido un error que requiere que se detenga la transmisión por secuencias.<br/>
<ul>
<li><em>Parám1</em>: <strong>HRESULT</strong> que indica el error que se ha producido.</li>
<li><em>Parám2</em>: no se usa.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>Especifica la cantidad de tiempo que tarda el presentador en representar cada fotograma. (Opcional).<br/>
<ul>
<li><em>Parám1</em>: puntero a un valor de <strong>LONGLONG</strong> constante que contiene la cantidad de tiempo que se va a procesar el marco, en unidades de 100-nanosegundos.</li>
<li><em>Parám2</em>: no se usa.</li>
</ul>
Para obtener más información, vea <a href="#processing-output">procesar la salida</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>Especifica el tiempo de retraso actual en los ejemplos de representación. Si el valor es positivo, los ejemplos están detrás de la programación. Si el valor es negativo, los ejemplos están por encima de la programación. (Opcional).<br/>
<ul>
<li><em>Parám1</em>: puntero a un valor de <strong>LONGLONG</strong> constante que contiene el tiempo de retardo, en unidades de 100-nanosegundos.</li>
<li><em>Parám2</em>: no se usa.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>Se envía inmediatamente después de <strong>EC_STEP_COMPLETE</strong> si la velocidad de reproducción es cero. Este evento contiene la marca de tiempo del marco que se mostró.<br/>
<ul>
<li><em>Parám1</em>: menos 32 bits de la marca de tiempo.</li>
<li><em>Parám2</em>: los 32 bits superiores de la marca de tiempo.</li>
</ul>
Para obtener más información, consulte <a href="#frame-stepping">recorrido de fotogramas</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>El presentador ha completado o cancelado un paso del marco.<br/>
<ul>
<li><em>Parám1</em>: no se utiliza.</li>
<li><em>Parám2</em>: no se usa.</li>
</ul>
Para obtener más información, consulte <a href="#frame-stepping">recorrido de fotogramas</a>.<br/>
<blockquote>
[!Note]<br />
Una versión anterior de la documentación que se describe en <em>parám1</em> incorrectamente. Este parámetro no se utiliza para este evento.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>Formatos de negociación

Siempre que el presentador recibe un mensaje **MFVP_MESSAGE_INVALIDATEMEDIATYPE** de EVR, debe establecer el formato de salida en el mezclador, como se indica a continuación:

1.  Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) en el mezclador para obtener un tipo de resultado posible. Este tipo describe un formato que el mezclador puede producir en función de los flujos de entrada y las capacidades de procesamiento de vídeo del dispositivo de gráficos.
2.  Compruebe si el presentador puede utilizar este tipo de medio como su formato de representación. Estos son algunos aspectos que se deben comprobar, aunque la implementación puede tener sus propios requisitos:

    -   El vídeo se debe descomprimir.
    -   El vídeo solo debe tener tramas progresivas. Compruebe que el atributo [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) sea igual a **MFVideoInterlace_Progressive**.
    -   El formato debe ser compatible con el dispositivo Direct3D.

    Si el tipo no es aceptable, vuelva al paso 1 y obtenga el siguiente tipo propuesto del mezclador.

3.  Cree un nuevo tipo de medio que sea un clon del tipo original y, a continuación, cambie los siguientes atributos:

    -   Establezca el atributo de [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) igual que el ancho y el alto que desee para las superficies de Direct3D que va a asignar.
    -   Establezca el atributo [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) en **false**.
    -   Establezca el atributo [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) igual que el par de la pantalla (normalmente 1:1).
    -   Establezca la abertura geométrica ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) atributo) igual a un rectángulo dentro de la superficie de Direct3D. Cuando el mezclador genera un fotograma de salida, blits la imagen de origen en este rectángulo. La abertura geométrica puede ser tan grande como la superficie o puede ser un subrectángulo dentro de la superficie. Para obtener más información, vea [rectángulos de origen y de destino](#source-and-destination-rectangles).

4.  Para probar si el mezclador va a aceptar el tipo de salida modificado, llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) con la marca **MFT_SET_TYPE_TEST_ONLY** . Si el mezclador rechaza el tipo, vuelva al paso 1 y obtenga el siguiente tipo.
5.  Asigne un grupo de superficies de Direct3D, tal como se describe en [asignación de superficies de Direct3D](#allocating-direct3d-surfaces). El mezclador usará estas superficies cuando dibuje los fotogramas de vídeo compuestos.
6.  Establezca el tipo de salida en el mezclador llamando a [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sin marcas. Si la primera llamada a **SetOutputType** se realizó correctamente en el paso 4, el método debería volver a tener éxito.

Si el mezclador se queda sin tipos, el método [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devuelve **MF_E_NO_MORE_TYPES**. Si el presentador no encuentra un tipo de salida adecuado para el mezclador, no se puede representar la secuencia. En ese caso, DirectShow o Media Foundation podrían intentar otro formato de secuencia. Por consiguiente, el presentador podría recibir varios mensajes de **MFVP_MESSAGE_INVALIDATEMEDIATYPE** en una fila hasta que se encuentre un tipo válido.

El mezclador realiza automáticamente la panorámica del vídeo, teniendo en cuenta la relación de aspecto de píxeles (PAR) del origen y el destino. Para obtener los mejores resultados, el ancho y el alto de la superficie y la abertura geométrica deben ser iguales al tamaño real en el que desea que aparezca el vídeo en la pantalla. En la imagen siguiente se ilustra este proceso.

![diagrama que muestra un fotogramas compuesto que conduce a una superficie de Direct3D, que conduce a una ventana](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

En el código siguiente se muestra el esquema del proceso. Algunos de los pasos se colocan en funciones auxiliares, los detalles exactos de los cuales dependerán de los requisitos del presentador.


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



Para obtener más información sobre los tipos de medios de vídeo, consulte [tipos de medios de vídeo](video-media-types.md).

## <a name="managing-the-direct3d-device"></a>Administrar el dispositivo Direct3D

El presentador crea el dispositivo Direct3D y controla cualquier pérdida de dispositivo durante el streaming. El presentador también hospeda el administrador de dispositivos de Direct3D, que proporciona una manera para que otros componentes usen el mismo dispositivo. Por ejemplo, el mezclador usa el dispositivo Direct3D para mezclar subsecuencias, Desentrelazar y realizar ajustes de color. Los descodificadores pueden usar el dispositivo Direct3D para la descodificación acelerada en vídeo. (Para obtener más información sobre la aceleración de vídeo, consulte [aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)).

Para configurar el dispositivo Direct3D, realice los pasos siguientes:

1.  Cree el objeto de Direct3D mediante una llamada a **Direct3DCreate9** o **Direct3DCreate9Ex**.
2.  Cree el dispositivo mediante una llamada a **IDirect3D9:: CreateDevice** o **IDirect3D9Ex:: CreateDevice**.
3.  Cree el administrador de dispositivos mediante una llamada a [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).
4.  Establezca el dispositivo en el administrador de dispositivos mediante una llamada a [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).

Si otro componente de canalización necesita el administrador de dispositivos, llama a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el EVR, especificando **MR_VIDEO_ACCELERATION_SERVICE** para el GUID de servicio. EVR pasa la solicitud al presentador. Una vez que el objeto obtiene el puntero [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , puede obtener un identificador para el dispositivo mediante una llamada a [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle). Cuando el objeto necesita usar el dispositivo, pasa el identificador del dispositivo al método [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , que devuelve un puntero **IDirect3DDevice9** .

Una vez creado el dispositivo, si el presentador destruye el dispositivo y crea uno nuevo, el presentador debe volver a llamar a [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) . El método **ResetDevice** invalida todos los identificadores de dispositivo existentes, lo que hace que [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) devuelva **DXVA2_E_NEW_VIDEO_DEVICE**. Este código de error señala a otros objetos mediante el dispositivo que deben abrir un nuevo identificador de dispositivo. Para obtener más información acerca del uso del administrador de dispositivos, consulte [Direct3D administrador de dispositivos](direct3d-device-manager.md).

El presentador puede crear el dispositivo en modo de ventana o en modo exclusivo de pantalla completa. En el modo de ventana, debe proporcionar una forma para que la aplicación especifique la ventana de vídeo. El presentador estándar implementa el método [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para este propósito. Debe crear el dispositivo cuando el presentador se cree por primera vez. Normalmente, no se sabrán todos los parámetros de dispositivo en este momento, como el formato de ventana o de búfer de reserva. Puede crear un dispositivo temporal y reemplazarlo más tarde&\# ; simplemente Recuerde llamar a [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) en el administrador de dispositivos.

Si crea un nuevo dispositivo, o si llama a **IDirect3DDevice9:: RESET** o **IDirect3DDevice9Ex:: ResetEx** en un dispositivo existente, envíe un evento [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) a EVR. Este evento notifica a EVR que vuelva a negociar el tipo de medio. EVR omite los parámetros de evento para este evento.

### <a name="allocating-direct3d-surfaces"></a>Asignación de superficies de Direct3D

Después de que el presentador establezca el tipo de medio, puede asignar las superficies de Direct3D, que el mezclador usará para escribir los fotogramas de vídeo. La superficie debe coincidir con el tipo de medio del presentador:

-   El formato de superficie debe coincidir con el subtipo de medio. Por ejemplo, si el subtipo es **MFVideoFormat_RGB24**, el formato de la superficie debe ser **D3DFMT_X8R8G8B8**. Para obtener más información sobre los subtipos y los formatos de Direct3D, vea [GUID de subtipo de vídeo](video-subtype-guids.md).
-   El ancho y el alto de la superficie deben coincidir con las dimensiones especificadas en el atributo [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) del tipo de medio.

La manera recomendada de asignar superficies depende de si el presentador se ejecuta en ventana o en pantalla completa.

Si el dispositivo Direct3D está en la ventana, puede crear varias cadenas de intercambio, cada una con un solo búfer de reserva. Con este enfoque, puede presentar cada superficie de forma independiente, ya que la presentación de una cadena de intercambio no interferirá con las demás cadenas de intercambio. El mezclador puede escribir datos en una superficie mientras otra superficie está programada para la presentación.

En primer lugar, decida cuántas cadenas de intercambio desea crear. Se recomienda un mínimo de tres. Para cada cadena de intercambio, haga lo siguiente:

1.  Llame a **IDirect3DDevice9:: CreateAdditionalSwapChain** para crear la cadena de intercambio.
2.  Llame a **IDirect3DSwapChain9:: GetBackBuffer** para obtener un puntero a la superficie del búfer de reserva de la cadena de intercambio.
3.  Llame a [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) y pase un puntero a la superficie. Esta función devuelve un puntero a un objeto de ejemplo de vídeo. El objeto de ejemplo de vídeo implementa la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) y el presentador usa esta interfaz para proporcionar la superficie al mezclador cuando el presentador llama al método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) de mixer. Para obtener más información sobre el objeto de ejemplo de vídeo, consulte [ejemplos de vídeo](video-samples.md).
4.  Almacene el puntero [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) en una cola. El presentador extraerá ejemplos de esta cola durante el procesamiento, tal y como se describe en [procesamiento de salida](#processing-output).
5.  Mantenga una referencia al puntero **IDirect3DSwapChain9** para que no se libere la cadena de intercambio.

En el modo exclusivo de pantalla completa, el dispositivo no puede tener más de una cadena de intercambio. Esta cadena de intercambio se crea implícitamente cuando se crea el dispositivo de pantalla completa. La cadena de intercambio puede tener más de un búfer de reserva. Desafortunadamente, sin embargo, si presenta un búfer de reserva mientras escribe en otro búfer de reserva en la misma cadena de intercambio, no hay ninguna manera fácil de coordinar las dos operaciones. Esto se debe a la manera en que Direct3D implementa el volteo de la superficie. Cuando se llama a Present, el controlador de gráficos actualiza los punteros de la superficie en la memoria de gráficos. Si está manteniendo los punteros de **IDirect3DSurface9** al llamar a **present**, apuntarán a distintos búferes después de que se devuelva la llamada **actual** .

La opción más sencilla consiste en crear un ejemplo de vídeo para la cadena de intercambio. Si elige esta opción, siga los mismos pasos indicados para el modo de ventana. La única diferencia es que la cola de ejemplo contiene una sola muestra de vídeo. Otra opción consiste en crear superficies ocultas y, a continuación, transformarlas en el búfer de reserva. Las superficies que cree deben admitir el método [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , que el mezclador usa para componer los fotogramas de salida.

### <a name="tracking-samples"></a>Ejemplos de seguimiento

Cuando el presentador asigna primero los ejemplos de vídeo, los coloca en una cola. El presentador dibuja desde esta cola cada vez que necesita obtener un nuevo fotograma del mezclador. Una vez que el mezclador envía el fotograma, el presentador mueve el ejemplo a una segunda cola. La segunda cola es para los ejemplos que están a la espera de los tiempos de presentación programados.

Para facilitar el seguimiento del estado de cada ejemplo, el objeto de ejemplo de vídeo implementa la interfaz [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) . Puede usar esta interfaz como se indica a continuación:

1.  Implemente la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) en el presentador.
2.  Antes de colocar un ejemplo en la cola programada, consulte el objeto de ejemplo de vídeo para la interfaz [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .

3.  Llame a [**IMFTrackedSample:: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) con un puntero a la interfaz de devolución de llamada.
4.  Cuando el ejemplo esté listo para su presentación, quítelo de la cola programada, preséntela y suelte todas las referencias al ejemplo.
5.  En el ejemplo se invoca la devolución de llamada. (El objeto de ejemplo no se elimina en este caso porque contiene un recuento de referencias en sí mismo hasta que se invoca la devolución de llamada).
6.  Dentro de la devolución de llamada, devuelva el ejemplo a la cola disponible.

No es necesario que un presentador use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) para realizar un seguimiento de los ejemplos; puede implementar cualquier técnica que funcione mejor para el diseño. Una ventaja de **IMFTrackedSample** es que puede trasladar las funciones de programación y representación del presentador a objetos auxiliares, y estos objetos no necesitan ningún mecanismo especial para volver a llamar al presentador cuando lanzan muestras de vídeo, ya que el objeto de ejemplo proporciona ese mecanismo.

En el código siguiente se muestra cómo establecer la devolución de llamada:


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



En la devolución de llamada, llame a [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) en el objeto de resultado asincrónico para recuperar un puntero al ejemplo:


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock **_/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /_*_ End lock _*_/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a>Procesar la salida

Siempre que el mezclador recibe un nuevo ejemplo de entrada, el EVR envía un mensaje _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY** al presentador. Este mensaje indica que el mezclador podría tener un nuevo fotograma de vídeo para entregarlo. En respuesta, el presentador llama a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador. Si el método se ejecuta correctamente, el presentador programa el ejemplo para la presentación.

Para obtener la salida del mezclador, realice los pasos siguientes:

1.  Compruebe el estado del reloj. Si el reloj está en pausa, pase por alto el mensaje de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** a menos que sea el primer fotograma de vídeo. Si el reloj se está ejecutando, o si se trata del primer fotograma de vídeo, continúe.
2.  Obtener un ejemplo de la cola de ejemplos disponibles. Si la cola está vacía, significa que todos los ejemplos asignados están programados actualmente para su presentación. En ese caso, omita el mensaje de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** en este momento. Cuando el siguiente ejemplo esté disponible, repita los pasos que se enumeran aquí.
3.  (Opcional). Si el reloj está disponible, obtenga la hora de reloj actual (*T1*) mediante una llamada a [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).
4.  Llame a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador. Si **ProcessOutput** se ejecuta correctamente, el ejemplo contiene un fotograma de vídeo. Si se produce un error en el método, compruebe el código de retorno. Los siguientes códigos de error de **ProcessOutput** no son errores críticos:

    

    | Código de error                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | El mezclador necesita más información para poder generar un nuevo fotograma de salida.<br/> Si obtiene este código de error, compruebe si EVR ha alcanzado el final de la secuencia y responda según corresponda, como se describe en [final de la secuencia](#end-of-stream). De lo contrario, pase por alto este mensaje **MF_E_TRANSFORM_NEED_MORE_INPUT** . El EVR enviará otro cuando el mezclador Obtenga más entradas.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | El tipo de salida del mezclador ha dejado de ser válido, posiblemente debido a un cambio de formato ascendente.<br/> Si obtiene este código de error, establezca el tipo de medio del presentador en **null**. El EVR solicitará un nuevo formato.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | El mezclador requiere un nuevo tipo de medio.<br/> Si obtiene este código de error, renegocie el tipo de salida del mezclador como se describe en [negociar formatos](#negotiating-formats).<br/>                                                                                                                                                                                                        |

    

     

    Si [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) se ejecuta correctamente, continúe.

5.  (Opcional). Si el reloj está disponible, obtenga la hora actual del reloj (*T2*). La cantidad de latencia introducida por el mezclador es (*T2*  -  *T1*). Envíe un evento de **EC_PROCESSING_LATENCY** con este valor a EVR. EVR usa este valor para el control de calidad. Si no hay ningún reloj disponible, no hay ningún motivo para enviar el evento de **EC_PROCESSING_LATENCY** .
6.  (Opcional). Consulte el ejemplo de [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) y llame a [**IMFTrackedSample:: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) tal y como se describe en [ejemplos de seguimiento](#tracking-samples).
7.  Programe el ejemplo para la presentación.

Esta secuencia de pasos puede finalizar antes de que el presentador obtenga cualquier salida del mezclador. Para asegurarse de que no se quita ninguna solicitud, debe repetir los mismos pasos cuando se produzca lo siguiente:

-   Se llama al método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o **IMFClockStateSink:: OnClockStart** del presentador. Esto controla el caso en el que el mezclador omite la entrada porque el reloj está en pausa (paso 1).
-   Se invoca la devolución de llamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) . Esto controla el caso en el que el mezclador recibe la entrada, pero todas las muestras de vídeo del presentador están en uso (paso 2).

En los siguientes ejemplos de código se muestran estos pasos con más detalle. El presentador llama al `ProcessInputNotify` método (que se muestra en el ejemplo siguiente) cuando obtiene el mensaje de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



Este `ProcessInputNotify` método establece una marca booleana para registrar el hecho de que el mezclador tiene una entrada nueva. A continuación, llama al `ProcessOutputLoop` método, que se muestra en el ejemplo siguiente. Este método intenta extraer tantas muestras como sea posible del mezclador:


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



El `ProcessOutput` método, que se muestra en el ejemplo siguiente, intenta obtener un único fotograma de vídeo del mezclador. Si no hay ningún fotograma de vídeo disponible, `ProcessSample` devuelve S_FALSE o un código de error, cualquiera de los cuales interrumpe el bucle en `ProcessOutputLoop` . La mayor parte del trabajo se realiza dentro del `ProcessOutput` método:


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



Algunos comentarios sobre este ejemplo:

-   Se supone que la variable *m_SamplePool* es un objeto de colección que contiene la cola de ejemplos de vídeo disponibles. El método del objeto `GetSample` devuelve **MF_E_SAMPLEALLOCATOR_EMPTY** si la cola está vacía.
-   Si el método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador devuelve MF_E_TRANSFORM_NEED_MORE_INPUT, significa que el mezclador no puede producir ningún resultado más, por lo que el presentador borra la marca *m_fSampleNotify* .
-   El `TrackSample` método, que establece la devolución de llamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , se muestra en la sección de [ejemplos de seguimiento](#tracking-samples).

### <a name="repainting-frames"></a>Volver a dibujar marcos

En ocasiones, es posible que el presentador tenga que volver a pintar el fotograma de vídeo más reciente. Por ejemplo, el presentador estándar vuelve a dibujar el marco en las siguientes situaciones:

-   En modo de ventana, en respuesta a **WM_PAINT** mensajes recibidos por la ventana de la aplicación. Vea [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   Si el rectángulo de destino cambia cuando la aplicación llama a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Siga estos pasos para solicitar al mezclador que vuelva a crear el fotograma más reciente:

1.  Obtener un ejemplo de vídeo de la cola.
2.  Consulte el ejemplo de la interfaz [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .
3.  Llame a [**IMFDesiredSample:: SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration). Especifique la marca de tiempo del fotograma de vídeo más reciente. (Tendrá que almacenar en caché este valor y actualizarlo para cada fotograma).
4.  Llame a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el mezclador.

Al volver a pintar un fotograma, puede omitir el reloj de la presentación y presentar el marco inmediatamente.

### <a name="scheduling-samples"></a>Ejemplos de programación

Los fotogramas de vídeo pueden alcanzar el EVR en cualquier momento. El presentador es responsable de presentar cada fotograma en el momento correcto, en función de la marca de tiempo del marco. Cuando el presentador obtiene un nuevo ejemplo del mezclador, coloca el ejemplo en la cola programada. En un subproceso independiente, el presentador obtiene continuamente la primera muestra del encabezado de la cola y determina si:

-   Presente el ejemplo.
-   Mantenga el ejemplo en la cola porque es pronto.
-   Descarte el ejemplo porque está retrasado. Aunque debe evitar la eliminación de fotogramas si es posible, es posible que necesite si el presentador está continuamente por detrás.

Para obtener la marca de tiempo de un fotograma de vídeo, llame a [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) en el ejemplo de vídeo. La marca de tiempo es relativa al reloj de presentación de EVR. Para obtener la hora actual del reloj, llame a [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime). Si el EVR no tiene un reloj de presentación o si un ejemplo no tiene una marca de tiempo, puede presentar el ejemplo inmediatamente después de obtenerlo.

Para obtener la duración de cada ejemplo, llame a [**IMFSample:: GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration). Si el ejemplo no tiene una duración, puede usar la función [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) para calcular la duración a partir de la velocidad de fotogramas.

Al programar ejemplos, tenga en cuenta lo siguiente:

-   Si la velocidad de reproducción es más rápida o más lenta que la velocidad normal, el reloj se ejecuta a una velocidad mayor o menor. Esto significa que la marca de tiempo de una muestra siempre proporciona el tiempo de destino correcto en relación con el reloj de la presentación. Sin embargo, si traduce los tiempos de presentación en otro tiempo de reloj (por ejemplo, el contador de rendimiento de alta resolución), debe escalar las horas en función de la velocidad del reloj. Si cambia la velocidad del reloj, EVR llama al método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del presentador.
-   La velocidad de reproducción puede ser negativa para la reproducción inversa. Cuando la velocidad de reproducción es negativa, el reloj de la presentación se ejecuta hacia atrás. En otras palabras, el tiempo *n* + 1 se produce antes de la hora *n*.

En el ejemplo siguiente se calcula la antelación o la finalización de un ejemplo, en relación con el reloj de la presentación:


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



El reloj del sistema o el procesador de audio normalmente controla el reloj de la presentación. (El representador de audio deriva el tiempo desde la velocidad a la que la tarjeta de sonido consume audio). En general, el reloj de la presentación no se sincroniza con la frecuencia de actualización del monitor.

Si los parámetros de presentación de Direct3D especifican **D3DPRESENT_INTERVAL_DEFAULT** o **D3DPRESENT_INTERVAL_ONE** para el intervalo de presentación, la operación **present** espera el reseguimiento vertical del monitor. Esta es una manera fácil de evitar el desgarro, pero reduce la precisión del algoritmo de programación. Por el contrario, si el intervalo de presentación es **D3DPRESENT_INTERVAL_IMMEDIATE**, el método **actual** se ejecuta inmediatamente, lo que provoca que se corte a menos que el algoritmo de programación sea lo suficientemente preciso como para que llame a **present** solo durante el período de reseguimiento vertical.

Las siguientes funciones pueden ayudarle a obtener información de tiempo precisa:

-   **IDirect3DDevice9:: GetRasterStatus** devuelve información sobre la trama, incluida la línea de exploración actual y si la trama está en el período en blanco vertical.
-   **DwmGetCompositionTimingInfo** devuelve información de tiempo para el administrador de ventanas de escritorio. Esta información es útil si la composición del escritorio está habilitada.

### <a name="presenting-samples"></a>Presentar ejemplos

En esta sección se supone que ha creado una cadena de intercambio independiente para cada superficie, tal como se describe en [asignación de superficies de Direct3D](#allocating-direct3d-surfaces). Para presentar un ejemplo, obtenga la cadena de intercambio del ejemplo de vídeo como se indica a continuación:

1.  Llame a [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) en el ejemplo de vídeo para obtener el búfer.
2.  Consulte el búfer para la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
3.  Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener la interfaz **IDirect3DSurface9** de la superficie de Direct3D. (Puede combinar este paso y el paso anterior en uno llamando a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)).
4.  Llame a **IDirect3DSurface9:: GetContainer** en la superficie para obtener un puntero a la cadena de intercambio.
5.  Llame a **IDirect3DSwapChain9::P reenviar** en la cadena de intercambio.

El siguiente código muestra estos pasos:


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a>Rectángulos de origen y de destino

El *rectángulo de origen* es la parte del fotograma de vídeo que se va a mostrar. Se define en relación con un sistema de coordenadas normalizado, en el que todo el fotograma de vídeo ocupa un rectángulo con las coordenadas {0, 0, 1, 1}. El *rectángulo de destino* es el área de la superficie de destino donde se dibuja el fotograma de vídeo. El presentador estándar permite a una aplicación establecer estos rectángulos mediante una llamada a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Hay varias opciones para aplicar los rectángulos de origen y de destino. La primera opción es dejar que el mezclador las aplique:

-   Establezca el rectángulo de origen mediante el atributo [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) . El mezclador aplicará el rectángulo de origen cuando blits el vídeo a la superficie de destino. El rectángulo de origen predeterminado del mezclador es todo el marco.
-   Establezca el rectángulo de destino como la abertura geométrica en el tipo de salida del mezclador. Para obtener más información, vea [negociar formatos](#negotiating-formats).

La segunda opción consiste en aplicar los rectángulos al **IDirect3DSwapChain9::P reenviar** especificando los parámetros *pSourceRect* y *pDestRect* en el método **present** . Puede combinar estas opciones. Por ejemplo, podría establecer el rectángulo de origen en el mezclador, pero aplicar el rectángulo de destino en el método **actual** .

Si la aplicación cambia el rectángulo de destino o cambia el tamaño de la ventana, es posible que tenga que asignar nuevas superficies. Si es así, debe tener cuidado de sincronizar esta operación con el subproceso de programación. Vacíe la cola de programación y descarte los ejemplos anteriores antes de asignar nuevas superficies.

### <a name="end-of-stream"></a>Final de la secuencia

Cuando finaliza cada flujo de entrada en el EVR, el EVR envía un mensaje de **MFVP_MESSAGE_ENDOFSTREAM** al presentador. Sin embargo, cuando reciba el mensaje, es posible que haya algunos fotogramas de vídeo pendientes de procesamiento. Antes de responder al mensaje de final de secuencia, debe purgar todos los resultados del mezclador y presentar todos los marcos restantes. Después de presentar el último fotograma, envíe un evento de **EC_COMPLETE** a EVR.

En el ejemplo siguiente se muestra un método que envía el evento **EC_COMPLETE** si se cumplen varias condiciones. De lo contrario, Devuelve S_OK sin enviar el evento:


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



Este método comprueba los Estados siguientes:

-   Si la variable de *m_fSampleNotify* es **true**, significa que el mezclador tiene uno o varios fotogramas que aún no se han procesado. (Para obtener más información, consulte [procesar la salida](#processing-output)).
-   La variable *m_fEndStreaming* es una marca booleana cuyo valor inicial es **false**. El presentador establece la marca en **true** cuando EVR envía el mensaje de **MFVP_MESSAGE_ENDOFSTREAM** .
-   `AreSamplesPending`Se supone que el método devuelve **true** siempre que uno o varios fotogramas estén esperando en la cola programada.

En el método [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) , establezca *m_fEndStreaming* en **true** y llame a `CheckEndOfStream` cuando EVR envíe el mensaje **MFVP_MESSAGE_ENDOFSTREAM** :


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Además, llame a `CheckEndOfStream` si el método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mezclador devuelve **MF_E_TRANSFORM_NEED_MORE_INPUT**. Este código de error indica que el mezclador no tiene más ejemplos de entrada (vea la [salida de procesamiento](#processing-output)).

## <a name="frame-stepping"></a>Recorrido de fotogramas

La EVR está diseñada para admitir la ejecución de fotogramas en DirectShow y la limpieza en Media Foundation. El recorrido y la limpieza de fotogramas son conceptualmente similares. En ambos casos, la aplicación solicita un fotograma de vídeo cada vez. Internamente, el presentador utiliza el mismo mecanismo para implementar ambas características.

La ejecución paso a paso en DirectShow funciona de la siguiente manera:

-   La aplicación llama a [**IVideoFrameStep:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step). El número de pasos se proporciona en el parámetro *dwSteps* . El EVR envía un mensaje de **MFVP_MESSAGE_STEP** al presentador, donde el parámetro de mensaje (*ulParam*) es el número de pasos.
-   Si la aplicación llama a [**IVideoFrameStep:: CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) o cambia el estado del gráfico (en ejecución, en pausa o detenido), EVR envía un mensaje de **MFVP_MESSAGE_CANCELSTEP** .

La limpieza en Media Foundation funciona de la siguiente manera:

-   La aplicación establece la velocidad de reproducción en cero llamando a [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).
-   Para representar un nuevo marco, la aplicación llama a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posición deseada. EVR envía un mensaje de **MFVP_MESSAGE_STEP** con *ulParam* igual a 1.
-   Para detener la limpieza, la aplicación establece la velocidad de reproducción en un valor distinto de cero. EVR envía el mensaje de **MFVP_MESSAGE_CANCELSTEP** .

Después de recibir el mensaje de **MFVP_MESSAGE_STEP** , el presentador espera a que llegue el marco de destino. Si el número de pasos es *N*, el presentador descarta los siguientes (*N* -1) ejemplos y presenta el ejemplo *N* . Cuando el presentador completa el paso del marco, envía un evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) a EVR con *LParam1* establecido en **false**. Además, si la velocidad de reproducción es cero, el presentador envía un evento [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) . Si el EVR cancela el recorrido de fotogramas mientras una operación de fotogramas sigue pendiente, el presentador envía un evento **EC_STEP_COMPLETE** con *LParam1* establecido en **true**.

La aplicación puede enmarcar el paso o borrar varias veces, por lo que el presentador podría recibir varios mensajes de **MFVP_MESSAGE_STEP** antes de que obtenga un mensaje **MFVP_MESSAGE_CANCELSTEP** . Además, el presentador puede recibir el mensaje de **MFVP_MESSAGE_STEP** antes de que se inicie el reloj o mientras se esté ejecutando el reloj.

### <a name="implementing-frame-stepping"></a>Implementación del recorrido de fotogramas

En esta sección se describe un algoritmo para implementar el recorrido de fotogramas. El algoritmo Stepping de fotogramas utiliza las siguientes variables:

-   *step_count*. Entero sin signo que especifica el número de pasos de la operación de recorrido del marco actual.
-   *step_queue*. Una cola de punteros [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
-   *step_state*. En cualquier momento, el presentador puede estar en uno de los siguientes Estados con respecto a la ejecución de fotogramas: 

    | Estado         | Descripción                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Sin recorrido de fotogramas.                                                                                                                                                                                             |
    | EN ESPERA       | El presentador ha recibido el mensaje de **MFVP_MESSAGE_STEP** , pero el reloj no se ha iniciado.                                                                                                                  |
    | PENDING       | El presentador ha recibido el mensaje de **MFVP_MESSAGE_STEP** y se ha iniciado el reloj, pero el presentador está esperando recibir el marco de destino.                                                             |
    | REGULAR     | El presentador ha recibido el marco de destino y lo ha programado para su presentación, pero no se ha presentado el marco.                                                                                        |
    | FINALIZA      | El presentador ha presentado el marco de destino y ha enviado el evento de [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) y está esperando el siguiente **MFVP_MESSAGE_STEP** o **MFVP_MESSAGE_CANCELSTEP** mensaje. |

    

     

    Estos Estados son independientes de los Estados del presentador que aparecen en la sección [Estados del presentador](#presenter-states).

Los procedimientos siguientes se definen para el algoritmo de ejecución de fotogramas:

Procedimiento PrepareFrameStep

1.  *Step_count* de incremento.
2.  Establezca *step_state* en en espera.
3.  Si el reloj se está ejecutando, llame a StartFrameStep.

Procedimiento StartFrameStep

1.  Si *step_state* es igual a Waiting, establezca *step_state* en Pending. Para cada ejemplo en *step_queue*, llame a DeliverFrameStepSample.
2.  Si *step_state* es igual a NOT_STEPPING, quite cualquier ejemplo de *step_queue* y programe la presentación.

Procedimiento CompleteFrameStep

1.  Establezca *step_state* en completa.
2.  Envíe el evento EC_STEP_COMPLETE con *lParam1*  =  **false**.
3.  Si la velocidad de reloj es cero, envíe el evento **EC_SCRUB_TIME** con la hora de ejemplo.

Procedimiento DeliverFrameStepSample

1.  Si la tasa de reloj es cero y el tiempo de espera de ejemplo de *tiempo de ejemplo*  +    <  , descartará el ejemplo. Salir.
2.  Si *step_state* es igual a programado o completo, agregue el ejemplo a *step_queue*. Salir.
3.  Decremento *step_count*.
4.  Si *step_count* > 0, descarte el ejemplo. Salir.
5.  Si *step_state* es igual a Waiting, agregue el ejemplo a *step_queue*. Salir.
6.  Programe el ejemplo para la presentación.
7.  Establezca *step_state* en programado.

Procedimiento CancelFrameStep

1.  Establezca *step_state* en NOT_STEPPING
2.  Restablezca *step_count* en cero.
3.  Si el valor anterior de *step_state* estaba esperando, pendiente o programado, envíe EC_STEP_COMPLETE con *lParam1*  =  **true**.

Llame a estos procedimientos de la siguiente manera:



| Mensaje o método del presentador                                                   | Procedimiento           |
|-------------------------------------------------------------------------------|---------------------|
| Mensaje **MFVP_MESSAGE_STEP**                                               | `PrepareFrameStep`  |
| Mensaje **MFVP_MESSAGE_STEP**                                               | `CancelStep`        |
| [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| Devolución de llamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)                         | `CompleteFrameStep` |
| [**IMFClockStateSink::OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

En el diagrama de flujo siguiente se muestran los procedimientos de ejecución de fotogramas.

![diagrama de flujo que muestra las rutas de acceso que comienzan con el \- paso de mensaje mfvp \- y el \- mensaje mfvp \- processinputnotify y terminan en "State = Complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Establecer el presentador en el EVR

Después de implementar el presentador, el siguiente paso es configurar el EVR para usarlo.

### <a name="setting-the-presenter-in-directshow"></a>Establecer el presentador en DirectShow

En una aplicación de DirectShow, establezca el presentador en el EVR como se indica a continuación:

1.  Cree el filtro EVR llamando a **CoCreateInstance**. El CLSID es **CLSID_EnhancedVideoRenderer**.
2.  Agregue EVR al gráfico de filtro.
3.  Cree una instancia del presentador. El presentador puede admitir la creación de objetos COM estándar mediante **IClassFactory**, pero esto no es obligatorio.
4.  Consulte el filtro EVR para la interfaz [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
5.  Llame a [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

### <a name="setting-the-presenter-in-media-foundation"></a>Establecer el presentador en Media Foundation

En Media Foundation, tiene varias opciones, dependiendo de si crea el receptor de medios EVR o el objeto de activación EVR. Para obtener más información sobre los objetos de activación, vea [objetos de activación](activation-objects.md).

En el caso del receptor de medios EVR, haga lo siguiente:

1.  Llame a [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) para crear el receptor de medios.
2.  Cree una instancia del presentador.
3.  Consulte el receptor de medios EVR para la interfaz [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
4.  Llame a [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

Para el objeto de activación EVR, haga lo siguiente:

1.  Llame a [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear el objeto de activación.
2.  Establezca uno de los siguientes atributos en el objeto de activación: 

    | Atributo                                                                                                         | Descripción                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Puntero a un objeto de activación para el presentador.<br/> Con esta marca, debe proporcionar un objeto de activación para el presentador. El objeto de activación debe implementar la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID del presentador.<br/> Con esta marca, el presentador debe admitir la creación de objetos COM estándar mediante **IClassFactory**.<br/>                                                                                         |

    

     

3.  Opcionalmente, establezca el atributo [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) en el objeto de activación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> <dt>

[Ejemplo de EVRPresenter](evrpresenter-sample.md)
</dt> </dl>

 

 
