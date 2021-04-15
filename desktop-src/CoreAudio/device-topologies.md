---
description: Topologías de dispositivos
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Topologías de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539345"
---
# <a name="device-topologies"></a>Topologías de dispositivos

La [API DeviceTopology](devicetopology-api.md) ofrece a los clientes control sobre una variedad de funciones internas de adaptadores de audio a los que no se puede acceder a través de la [API de MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)o la [API de EndpointVolume](endpointvolume-api.md).

Como se explicó anteriormente, las API [MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)y [EndpointVolume](endpointvolume-api.md) presentan micrófonos, altavoces, auriculares y otros dispositivos de entrada y salida de audio a los clientes como dispositivos de [punto de conexión de audio](audio-endpoint-devices.md). El modelo de dispositivo de extremo proporciona a los clientes un acceso cómodo a los controles VOLUME y MUTE en los dispositivos de audio. Los clientes que solo requieren estos controles simples pueden evitar atravesar las topologías internas de los dispositivos de hardware en los adaptadores de audio.

En Windows Vista, el motor de audio configura automáticamente las topologías de dispositivos de audio para que las usen las aplicaciones de audio. Por lo tanto, las aplicaciones rara vez, si es necesario, deben usar la API de DeviceTopology para este propósito. Por ejemplo, supongamos que un adaptador de audio contiene un multiplexor de entrada que puede capturar una secuencia de una entrada de línea o un micrófono, pero que no puede capturar flujos de ambos dispositivos de extremo al mismo tiempo. Supongamos que el usuario ha habilitado las aplicaciones en modo exclusivo para tener preferencia sobre el uso de un dispositivo de punto de conexión de audio por parte de aplicaciones de modo compartido, como se describe en [flujos de modo exclusivo](exclusive-mode-streams.md). Si una aplicación de modo compartido está grabando una transmisión desde la entrada de línea en el momento en que una aplicación de modo exclusivo comienza a grabar un flujo desde el micrófono, el motor de audio cambia automáticamente el multiplexor de la entrada de línea al micrófono. Por el contrario, en versiones anteriores de Windows, incluida Windows XP, la aplicación en modo exclusivo de este ejemplo usaría las funciones **mixerXxx** en la API multimedia de Windows para atravesar las topologías de los dispositivos de adaptador, detectar el multiplexor y configurar el multiplexor para seleccionar la entrada del micrófono. En Windows Vista, ya no es necesario seguir estos pasos.

Sin embargo, es posible que algunos clientes requieran un control explícito sobre los tipos de controles de hardware de audio a los que no se puede acceder a través de la API MMDevice, WASAPI o la API EndpointVolume. Para estos clientes, la API DeviceTopology ofrece la posibilidad de atravesar las topologías de los dispositivos de adaptador para detectar y administrar los controles de audio en los dispositivos. Las aplicaciones que usan la API DeviceTopology deben diseñarse con cuidado para evitar interferir con la Directiva de audio de Windows y afectar a las configuraciones internas de los dispositivos de audio que se comparten con otras aplicaciones. Para obtener más información acerca de la Directiva de audio de Windows, consulte [componentes de audio de modo de usuario](user-mode-audio-components.md).

La API DeviceTopology proporciona interfaces para detectar y administrar los siguientes tipos de controles de audio en una topología de dispositivo:

-   Control de ganancia automática
-   Control de graves
-   Selector de entrada (multiplexor)
-   Control de sonoridad
-   Control de intervalo medio
-   Silenciar control
-   Selector de salida (demultiplexor)
-   Medidor de pico
-   Control de agudos
-   Control de volumen

Además, la API de DeviceTopology permite a los clientes consultar los dispositivos de adaptador para obtener información sobre los formatos de secuencia que admiten. El archivo de encabezado Devicetopology. h define las interfaces de la API de DeviceTopology.

En el diagrama siguiente se muestra un ejemplo de varias topologías de dispositivos conectados para la parte de un adaptador de PCI que captura audio de un micrófono, una entrada de línea y un reproductor de CD.

![ejemplo de cuatro topologías de dispositivo conectado](images/fig2.jpg)

En el diagrama anterior se muestran las rutas de acceso de datos que conducen de las entradas analógicas al bus del sistema. Cada uno de los siguientes dispositivos se representa como un objeto de topología de dispositivo con una interfaz [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :

-   Dispositivo de captura de onda
-   Dispositivo multiplexor de entrada
-   Dispositivo de extremo A
-   Dispositivo de extremo B

Tenga en cuenta que el diagrama de topología combina los dispositivos de adaptador (los dispositivos de captura de onda y multiplexor de entrada) con los dispositivos de punto de conexión. A través de las conexiones entre los dispositivos, los datos de audio pasan de un dispositivo a otro. En cada lado de una conexión hay un conector (etiquetado con en el diagrama) a través del cual los datos entran o salen de un dispositivo.

En el borde izquierdo del diagrama, las señales de los conectores de entrada de línea y micrófono entran en los dispositivos de extremo.

Dentro del dispositivo de captura de onda y el dispositivo multiplexor de entrada son funciones de procesamiento de transmisiones, que, en la terminología de la API DeviceTopology, se denominan subunidades. En el diagrama anterior aparecen los siguientes tipos de subunidades:

-   Control de volumen (con la etiqueta vol)
-   Silenciar control (etiquetar silencio)
-   Multiplexor (o selector de entrada; con la etiqueta MUX)
-   Convertidor de analógico a digital (con la etiqueta ADC)

Los clientes pueden controlar la configuración de las subunidades de volumen, silencio y multiplexor, y la API de DeviceTopology proporciona interfaces de control a los clientes para controlarlas. En este ejemplo, la subunidad de ADC no tiene ninguna configuración de control. Por lo tanto, la API de DeviceTopology no proporciona ninguna interfaz de control para el ADC.

En la terminología de la API de DeviceTopology, los conectores y las subunidades pertenecen a la misma categoría general: piezas. Todas las partes, independientemente de si son conectores o subunidades, proporcionan un conjunto común de funciones. La API de DeviceTopology implementa una interfaz [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) para representar las funciones genéricas que son comunes a los conectores y subunidades. La API implementa las interfaces [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) y [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) para representar los aspectos específicos de los conectores y las subunidades.

La API de DeviceTopology construye las topologías del dispositivo de captura de onda y el dispositivo multiplexor de entrada desde los filtros de streaming de kernel (KS) que el controlador de audio expone al sistema operativo para representar estos dispositivos. (El controlador del adaptador de audio implementa las interfaces **IMiniportWaveXxx** y **IMiniportTopology** para representar las partes dependientes del hardware de estos filtros; para obtener más información acerca de estas interfaces y sobre los filtros KS, consulte la documentación del DDK de Windows).

La API de DeviceTopology crea topologías triviales para representar los dispositivos de punto de conexión A y B en el diagrama anterior. La topología de dispositivo de un dispositivo de punto de conexión consta de un único conector. Esta topología es simplemente un marcador de posición para el dispositivo de punto de conexión y no contiene subunidades para procesar datos de audio. De hecho, los dispositivos de adaptador contienen todas las subunidades que las aplicaciones cliente utilizan para controlar el procesamiento de audio. La topología de dispositivo de un dispositivo de punto de conexión sirve principalmente como punto de partida para explorar las topologías de dispositivos de los dispositivos de adaptador.

Las conexiones internas entre dos partes de una topología de dispositivo se denominan vínculos. La API DeviceTopology proporciona métodos para atravesar vínculos de una parte a la siguiente en una topología de dispositivo. La API también proporciona métodos para atravesar las conexiones entre topologías de dispositivos.

Para comenzar la exploración de un conjunto de topologías de dispositivo conectado, una aplicación cliente activa la interfaz **IDeviceTopology** de un dispositivo de punto de conexión de audio. El conector de un dispositivo de extremo se conecta a un conector en un adaptador de audio o en una red. Si el extremo se conecta a un dispositivo en un adaptador de audio, los métodos de la API de DeviceTopology permiten a la aplicación recorrer la conexión desde el extremo al adaptador obteniendo una referencia a la interfaz **IDeviceTopology** del dispositivo adaptador en el otro lado de la conexión. Por otro lado, una red no tiene ninguna topología de dispositivo. Una conexión de red canaliza una secuencia de audio a un cliente que tiene acceso al sistema de forma remota.

La API DeviceTopology proporciona acceso únicamente a las topologías de los dispositivos de hardware en un adaptador de audio. Los dispositivos externos en el borde izquierdo del diagrama y los componentes de software del borde derecho quedan fuera del ámbito de la API. Las líneas discontinuas de cada lado del diagrama representan los límites de la API de DeviceTopology. El cliente puede usar la API para explorar una ruta de acceso de datos que se estira del conector de entrada al bus del sistema, pero la API no puede penetrar más allá de estos límites.

Cada conector del diagrama anterior tiene asociado un tipo de conexión que indica el tipo de conexión que realiza el conector. Por lo tanto, los conectores de los dos lados de una conexión siempre tienen tipos de conexión idénticos. El tipo de conexión se indica mediante un valor de enumeración [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) ( \_ externa física, \_ interna física, software \_ fijo, \_ e/s de software o red). Las conexiones entre el dispositivo de multiplexor de entrada y los dispositivos de punto de conexión A y B son del tipo \_ externo físico, lo que significa que la conexión representa una conexión física a un dispositivo externo (es decir, un conector de audio accesible desde el usuario). La conexión a la señal analógica del reproductor de CD interno es del tipo \_ interno físico, que indica una conexión física a un dispositivo auxiliar que se instala dentro del chasis del sistema. La conexión entre el dispositivo de captura de onda y el dispositivo multiplexor de entrada es de tipo software \_ fijo, que indica una conexión permanente que se ha corregido y no se puede configurar en el control de software. Por último, la conexión al bus del sistema en el lado derecho del diagrama es de tipo e/s de software \_ , que indica que un motor DMA implementa la e/s de datos para la conexión en el control de software. (El diagrama no incluye un ejemplo de un tipo de conexión de red).

El cliente comienza a atravesar una ruta de acceso de datos en el dispositivo de extremo. En primer lugar, el cliente obtiene una interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa el dispositivo de punto de conexión, como se explica en [enumerar dispositivos de audio](enumerating-audio-devices.md). Para obtener la interfaz **IDeviceTopology** para el dispositivo de extremo, el cliente llama al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el *IID* de parámetro establecido en REFIID IID \_ IDeviceTopology.

En el ejemplo del diagrama anterior, el dispositivo multiplexor de entrada contiene todos los controles de hardware (volumen, silencio y multiplexor) de las secuencias de captura de los conectores de entrada de línea y micrófono. En el ejemplo de código siguiente se muestra cómo obtener la interfaz **IDeviceTopology** para el dispositivo multiplexor de entrada desde la interfaz **IMMDevice** para el dispositivo de extremo para la entrada de línea o el micrófono:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



En la función GetHardwareDeviceTopology del ejemplo de código anterior se realizan los pasos siguientes para obtener la interfaz **IDeviceTopology** para el dispositivo multiplexor de entrada:

1.  Llame al método **IMMDevice:: Activate** para obtener la interfaz **IDeviceTopology** para el dispositivo de extremo.
2.  Con la interfaz **IDeviceTopology** obtenida en el paso anterior, llame al método [**IDeviceTopology:: GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) para obtener la interfaz **IConnector** del conector único (número de conector 0) en el dispositivo de extremo.
3.  Con la interfaz **IConnector** obtenida en el paso anterior, llame al método [**IConnector:: GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) para obtener la interfaz **IConnector** del conector en el dispositivo multiplexor de entrada.
4.  Consulte la interfaz **IConnector** obtenida en el paso anterior para su interfaz **IPart** .
5.  Con la interfaz **IPart** obtenida en el paso anterior, llame al método [**IPart:: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) para obtener la interfaz **IDeviceTopology** para el dispositivo multiplexor de entrada.

Antes de que el usuario pueda grabar desde el micrófono en el diagrama anterior, la aplicación cliente debe asegurarse de que el multiplexor selecciona la entrada del micrófono. En el ejemplo de código siguiente se muestra cómo un cliente puede atravesar la ruta de acceso de datos del micrófono hasta que encuentra el multiplexor, que después programa para seleccionar la entrada del micrófono:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



La API de DeviceTopology implementa una interfaz [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) para encapsular un multiplexor, como el del diagrama anterior. (Una interfaz [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) encapsula un demultiplexador). En el ejemplo de código anterior, el bucle interno de la función SelectCaptureDevice consulta cada subunidad que encuentra para detectar si la subunidad es un multiplexor. Si la subunidad es un multiplexor, la función llama al método [**IAudioInputSelector:: SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) para seleccionar la entrada que se conecta a la secuencia desde el dispositivo de extremo.

En el ejemplo de código anterior, cada iteración del bucle exterior atraviesa una topología de dispositivo. Al atravesar las topologías del dispositivo en el diagrama anterior, la primera iteración atraviesa el dispositivo multiplexor de entrada y la segunda iteración atraviesa el dispositivo de captura de onda. La función terminará cuando llegue al conector en el borde derecho del diagrama. La terminación se produce cuando la función detecta un conector con un \_ tipo de conexión de e/s de software. Este tipo de conexión identifica el punto en el que el dispositivo de adaptador se conecta al bus de sistema.

La llamada al método [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) en el ejemplo de código anterior obtiene un valor de enumeración **IPartType** que indica si la parte actual es un conector o una subunidad de procesamiento de audio.

El bucle interno en el ejemplo de código anterior recorre el vínculo de una parte a la siguiente llamando al método [**IPart:: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) . (También hay un método [**IPart:: EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) para la ejecución paso a paso en la dirección opuesta). Este método recupera un objeto [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) que contiene una lista de todos los elementos salientes. Sin embargo, cualquier parte que la función SelectCaptureDevice espera encontrar en un dispositivo de captura siempre tendrá exactamente un elemento saliente. Por lo tanto, la siguiente llamada a [**IPartsList:: getPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) siempre solicita la primera parte de la lista, el número de parte 0, porque la función supone que se trata de la única parte de la lista.

Si la función SelectCaptureDevice encuentra una topología para la que esa suposición no es válida, es posible que la función no pueda configurar correctamente el dispositivo. Para evitar este tipo de error, una versión más general de la función podría hacer lo siguiente:

-   Llame al método [**IPartsList:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) para determinar el número de elementos salientes.
-   Para cada elemento saliente, llame a **IPartsList:: getPart** para empezar a atravesar la ruta de acceso de datos que conduce desde la parte.

Algunos de los elementos, pero no necesariamente todos, tienen controles de hardware asociados que los clientes pueden establecer u obtener. Una parte determinada puede tener cero, uno o más controles de hardware. Un control de hardware se representa mediante el siguiente par de interfaces:

-   Una interfaz de control genérico, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), que tiene métodos comunes a todos los controles de hardware.
-   Una interfaz específica de la función (por ejemplo, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) que expone los parámetros de control para un tipo determinado de control de hardware (por ejemplo, un control de volumen).

Para enumerar los controles de hardware de un elemento, el cliente llama primero al método [**IPart:: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) para determinar el número de controles de hardware que están asociados a la parte. Después, el cliente realiza una serie de llamadas al método [**IPart:: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) para obtener la interfaz **IControlInterface** para cada control de hardware. Por último, el cliente obtiene la interfaz específica de la función para cada control de hardware llamando al método [**IControlInterface:: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) para obtener el identificador de interfaz. El cliente llama al método [**IPart:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) con este identificador para obtener la interfaz específica de la función.

Una parte que es un conector podría admitir una de las siguientes interfaces de control específicas de la función:

-   [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

Una parte que es una subunidad podría admitir una o varias de las siguientes interfaces de control específicas de la función:

-   [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

Un elemento admite la interfaz **IDeviceSpecificProperty** solo si el control de hardware subyacente tiene un valor de control específico del dispositivo y el control no se puede representar de forma adecuada con ninguna otra interfaz específica de la función de la lista anterior. Normalmente, una propiedad específica del dispositivo solo es útil para un cliente que puede inferir el significado del valor de propiedad a partir de información como el tipo de elemento, el subtipo de elemento y el nombre de la parte. El cliente puede obtener esta información mediante una llamada a los métodos [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)y [**IPart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 
