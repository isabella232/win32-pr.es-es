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
# <a name="device-topologies"></a><span data-ttu-id="bf92c-103">Topologías de dispositivos</span><span class="sxs-lookup"><span data-stu-id="bf92c-103">Device Topologies</span></span>

<span data-ttu-id="bf92c-104">La [API DeviceTopology](devicetopology-api.md) ofrece a los clientes control sobre una variedad de funciones internas de adaptadores de audio a los que no se puede acceder a través de la [API de MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)o la [API de EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="bf92c-104">The [DeviceTopology API](devicetopology-api.md) gives clients control over a variety of internal functions of audio adapters that they cannot access through the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), or the [EndpointVolume API](endpointvolume-api.md).</span></span>

<span data-ttu-id="bf92c-105">Como se explicó anteriormente, las API [MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)y [EndpointVolume](endpointvolume-api.md) presentan micrófonos, altavoces, auriculares y otros dispositivos de entrada y salida de audio a los clientes como dispositivos de [punto de conexión de audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="bf92c-105">As explained previously, the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), and the [EndpointVolume API](endpointvolume-api.md) present microphones, speakers, headphones, and other audio input and output devices to clients as [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="bf92c-106">El modelo de dispositivo de extremo proporciona a los clientes un acceso cómodo a los controles VOLUME y MUTE en los dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-106">The endpoint device model provides clients with convenient access to volume and mute controls in audio devices.</span></span> <span data-ttu-id="bf92c-107">Los clientes que solo requieren estos controles simples pueden evitar atravesar las topologías internas de los dispositivos de hardware en los adaptadores de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-107">Clients that require only these simple controls can avoid traversing the internal topologies of hardware devices in audio adapters.</span></span>

<span data-ttu-id="bf92c-108">En Windows Vista, el motor de audio configura automáticamente las topologías de dispositivos de audio para que las usen las aplicaciones de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-108">In Windows Vista, the audio engine automatically configures the topologies of audio devices for use by audio applications.</span></span> <span data-ttu-id="bf92c-109">Por lo tanto, las aplicaciones rara vez, si es necesario, deben usar la API de DeviceTopology para este propósito.</span><span class="sxs-lookup"><span data-stu-id="bf92c-109">Thus, applications rarely, if ever, need to use the DeviceTopology API for this purpose.</span></span> <span data-ttu-id="bf92c-110">Por ejemplo, supongamos que un adaptador de audio contiene un multiplexor de entrada que puede capturar una secuencia de una entrada de línea o un micrófono, pero que no puede capturar flujos de ambos dispositivos de extremo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-110">For example, assume that an audio adapter contains an input multiplexer that can capture a stream from either a line input or a microphone, but that cannot capture streams from both endpoint devices at the same time.</span></span> <span data-ttu-id="bf92c-111">Supongamos que el usuario ha habilitado las aplicaciones en modo exclusivo para tener preferencia sobre el uso de un dispositivo de punto de conexión de audio por parte de aplicaciones de modo compartido, como se describe en [flujos de modo exclusivo](exclusive-mode-streams.md).</span><span class="sxs-lookup"><span data-stu-id="bf92c-111">Assume that the user has enabled exclusive-mode applications to preempt the use of an audio endpoint device by shared-mode applications, as described in [Exclusive-Mode Streams](exclusive-mode-streams.md).</span></span> <span data-ttu-id="bf92c-112">Si una aplicación de modo compartido está grabando una transmisión desde la entrada de línea en el momento en que una aplicación de modo exclusivo comienza a grabar un flujo desde el micrófono, el motor de audio cambia automáticamente el multiplexor de la entrada de línea al micrófono.</span><span class="sxs-lookup"><span data-stu-id="bf92c-112">If a shared-mode application is recording a stream from the line input at the time that an exclusive-mode application begins recording a stream from the microphone, the audio engine automatically switches the multiplexer from the line input to the microphone.</span></span> <span data-ttu-id="bf92c-113">Por el contrario, en versiones anteriores de Windows, incluida Windows XP, la aplicación en modo exclusivo de este ejemplo usaría las funciones **mixerXxx** en la API multimedia de Windows para atravesar las topologías de los dispositivos de adaptador, detectar el multiplexor y configurar el multiplexor para seleccionar la entrada del micrófono.</span><span class="sxs-lookup"><span data-stu-id="bf92c-113">In contrast, in earlier versions of Windows, including Windows XP, the exclusive-mode application in this example would use the **mixerXxx** functions in the Windows multimedia API to traverse the topologies of the adapter devices, discover the multiplexer, and configure the multiplexer to select the microphone input.</span></span> <span data-ttu-id="bf92c-114">En Windows Vista, ya no es necesario seguir estos pasos.</span><span class="sxs-lookup"><span data-stu-id="bf92c-114">In Windows Vista, these steps are no longer required.</span></span>

<span data-ttu-id="bf92c-115">Sin embargo, es posible que algunos clientes requieran un control explícito sobre los tipos de controles de hardware de audio a los que no se puede acceder a través de la API MMDevice, WASAPI o la API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="bf92c-115">However, some clients might require explicit control over types of audio hardware controls that cannot be accessed through the MMDevice API, WASAPI, or the EndpointVolume API.</span></span> <span data-ttu-id="bf92c-116">Para estos clientes, la API DeviceTopology ofrece la posibilidad de atravesar las topologías de los dispositivos de adaptador para detectar y administrar los controles de audio en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bf92c-116">For these clients, the DeviceTopology API provides the ability to traverse the topologies of adapter devices to discover and manage the audio controls in the devices.</span></span> <span data-ttu-id="bf92c-117">Las aplicaciones que usan la API DeviceTopology deben diseñarse con cuidado para evitar interferir con la Directiva de audio de Windows y afectar a las configuraciones internas de los dispositivos de audio que se comparten con otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bf92c-117">Applications that use the DeviceTopology API must be designed with care to avoid interfering with Windows audio policy and disturbing the internal configurations of audio devices that are shared with other applications.</span></span> <span data-ttu-id="bf92c-118">Para obtener más información acerca de la Directiva de audio de Windows, consulte [componentes de audio de modo de usuario](user-mode-audio-components.md).</span><span class="sxs-lookup"><span data-stu-id="bf92c-118">For more information about Windows audio policy, see [User-Mode Audio Components](user-mode-audio-components.md).</span></span>

<span data-ttu-id="bf92c-119">La API DeviceTopology proporciona interfaces para detectar y administrar los siguientes tipos de controles de audio en una topología de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="bf92c-119">The DeviceTopology API provides interfaces for discovering and managing the following types of audio controls in a device topology:</span></span>

-   <span data-ttu-id="bf92c-120">Control de ganancia automática</span><span class="sxs-lookup"><span data-stu-id="bf92c-120">Automatic gain control</span></span>
-   <span data-ttu-id="bf92c-121">Control de graves</span><span class="sxs-lookup"><span data-stu-id="bf92c-121">Bass control</span></span>
-   <span data-ttu-id="bf92c-122">Selector de entrada (multiplexor)</span><span class="sxs-lookup"><span data-stu-id="bf92c-122">Input selector (multiplexer)</span></span>
-   <span data-ttu-id="bf92c-123">Control de sonoridad</span><span class="sxs-lookup"><span data-stu-id="bf92c-123">Loudness control</span></span>
-   <span data-ttu-id="bf92c-124">Control de intervalo medio</span><span class="sxs-lookup"><span data-stu-id="bf92c-124">Midrange control</span></span>
-   <span data-ttu-id="bf92c-125">Silenciar control</span><span class="sxs-lookup"><span data-stu-id="bf92c-125">Mute control</span></span>
-   <span data-ttu-id="bf92c-126">Selector de salida (demultiplexor)</span><span class="sxs-lookup"><span data-stu-id="bf92c-126">Output selector (demultiplexer)</span></span>
-   <span data-ttu-id="bf92c-127">Medidor de pico</span><span class="sxs-lookup"><span data-stu-id="bf92c-127">Peak meter</span></span>
-   <span data-ttu-id="bf92c-128">Control de agudos</span><span class="sxs-lookup"><span data-stu-id="bf92c-128">Treble control</span></span>
-   <span data-ttu-id="bf92c-129">Control de volumen</span><span class="sxs-lookup"><span data-stu-id="bf92c-129">Volume control</span></span>

<span data-ttu-id="bf92c-130">Además, la API de DeviceTopology permite a los clientes consultar los dispositivos de adaptador para obtener información sobre los formatos de secuencia que admiten.</span><span class="sxs-lookup"><span data-stu-id="bf92c-130">In addition, the DeviceTopology API enables clients to query adapter devices for information about the stream formats that they support.</span></span> <span data-ttu-id="bf92c-131">El archivo de encabezado Devicetopology. h define las interfaces de la API de DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="bf92c-131">The header file Devicetopology.h defines the interfaces in the DeviceTopology API.</span></span>

<span data-ttu-id="bf92c-132">En el diagrama siguiente se muestra un ejemplo de varias topologías de dispositivos conectados para la parte de un adaptador de PCI que captura audio de un micrófono, una entrada de línea y un reproductor de CD.</span><span class="sxs-lookup"><span data-stu-id="bf92c-132">The following diagram shows an example of several connected device topologies for the portion of a PCI adapter that captures audio from a microphone, line input, and CD player.</span></span>

![ejemplo de cuatro topologías de dispositivo conectado](images/fig2.jpg)

<span data-ttu-id="bf92c-134">En el diagrama anterior se muestran las rutas de acceso de datos que conducen de las entradas analógicas al bus del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf92c-134">The preceding diagram shows the data paths that lead from the analog inputs to the system bus.</span></span> <span data-ttu-id="bf92c-135">Cada uno de los siguientes dispositivos se representa como un objeto de topología de dispositivo con una interfaz [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :</span><span class="sxs-lookup"><span data-stu-id="bf92c-135">Each of the following devices is represented as a device-topology object with an [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface:</span></span>

-   <span data-ttu-id="bf92c-136">Dispositivo de captura de onda</span><span class="sxs-lookup"><span data-stu-id="bf92c-136">Wave capture device</span></span>
-   <span data-ttu-id="bf92c-137">Dispositivo multiplexor de entrada</span><span class="sxs-lookup"><span data-stu-id="bf92c-137">Input multiplexer device</span></span>
-   <span data-ttu-id="bf92c-138">Dispositivo de extremo A</span><span class="sxs-lookup"><span data-stu-id="bf92c-138">Endpoint device A</span></span>
-   <span data-ttu-id="bf92c-139">Dispositivo de extremo B</span><span class="sxs-lookup"><span data-stu-id="bf92c-139">Endpoint device B</span></span>

<span data-ttu-id="bf92c-140">Tenga en cuenta que el diagrama de topología combina los dispositivos de adaptador (los dispositivos de captura de onda y multiplexor de entrada) con los dispositivos de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="bf92c-140">Note that the topology diagram combines adapter devices (the wave capture and input multiplexer devices) with endpoint devices.</span></span> <span data-ttu-id="bf92c-141">A través de las conexiones entre los dispositivos, los datos de audio pasan de un dispositivo a otro.</span><span class="sxs-lookup"><span data-stu-id="bf92c-141">Through the connections between devices, audio data passes from one device to the next.</span></span> <span data-ttu-id="bf92c-142">En cada lado de una conexión hay un conector (etiquetado con en el diagrama) a través del cual los datos entran o salen de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-142">On each side of a connection is a connector (labeled Con in the diagram) through which data enters or leaves a device.</span></span>

<span data-ttu-id="bf92c-143">En el borde izquierdo del diagrama, las señales de los conectores de entrada de línea y micrófono entran en los dispositivos de extremo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-143">On the left edge of the diagram, signals from the line-input and microphone jacks enter the endpoint devices.</span></span>

<span data-ttu-id="bf92c-144">Dentro del dispositivo de captura de onda y el dispositivo multiplexor de entrada son funciones de procesamiento de transmisiones, que, en la terminología de la API DeviceTopology, se denominan subunidades.</span><span class="sxs-lookup"><span data-stu-id="bf92c-144">Inside the wave capture device and input multiplexer device are stream-processing functions, which, in the terminology of the DeviceTopology API, are called subunits.</span></span> <span data-ttu-id="bf92c-145">En el diagrama anterior aparecen los siguientes tipos de subunidades:</span><span class="sxs-lookup"><span data-stu-id="bf92c-145">The following types of subunits appear in the preceding diagram:</span></span>

-   <span data-ttu-id="bf92c-146">Control de volumen (con la etiqueta vol)</span><span class="sxs-lookup"><span data-stu-id="bf92c-146">Volume control (labeled Vol)</span></span>
-   <span data-ttu-id="bf92c-147">Silenciar control (etiquetar silencio)</span><span class="sxs-lookup"><span data-stu-id="bf92c-147">Mute control (labeled Mute)</span></span>
-   <span data-ttu-id="bf92c-148">Multiplexor (o selector de entrada; con la etiqueta MUX)</span><span class="sxs-lookup"><span data-stu-id="bf92c-148">Multiplexer (or input selector; labeled MUX)</span></span>
-   <span data-ttu-id="bf92c-149">Convertidor de analógico a digital (con la etiqueta ADC)</span><span class="sxs-lookup"><span data-stu-id="bf92c-149">Analog-to-digital converter (labeled ADC)</span></span>

<span data-ttu-id="bf92c-150">Los clientes pueden controlar la configuración de las subunidades de volumen, silencio y multiplexor, y la API de DeviceTopology proporciona interfaces de control a los clientes para controlarlas.</span><span class="sxs-lookup"><span data-stu-id="bf92c-150">The settings in the volume, mute, and multiplexer subunits can be controlled by clients, and the DeviceTopology API provides control interfaces to clients for controlling them.</span></span> <span data-ttu-id="bf92c-151">En este ejemplo, la subunidad de ADC no tiene ninguna configuración de control.</span><span class="sxs-lookup"><span data-stu-id="bf92c-151">In this example, the ADC subunit has no control settings.</span></span> <span data-ttu-id="bf92c-152">Por lo tanto, la API de DeviceTopology no proporciona ninguna interfaz de control para el ADC.</span><span class="sxs-lookup"><span data-stu-id="bf92c-152">Thus, the DeviceTopology API provides no control interface for the ADC.</span></span>

<span data-ttu-id="bf92c-153">En la terminología de la API de DeviceTopology, los conectores y las subunidades pertenecen a la misma categoría general: piezas.</span><span class="sxs-lookup"><span data-stu-id="bf92c-153">In the terminology of the DeviceTopology API, connectors and subunits belong to the same general category—parts.</span></span> <span data-ttu-id="bf92c-154">Todas las partes, independientemente de si son conectores o subunidades, proporcionan un conjunto común de funciones.</span><span class="sxs-lookup"><span data-stu-id="bf92c-154">All parts, regardless of whether they are connectors or subunits, provide a common set of functions.</span></span> <span data-ttu-id="bf92c-155">La API de DeviceTopology implementa una interfaz [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) para representar las funciones genéricas que son comunes a los conectores y subunidades.</span><span class="sxs-lookup"><span data-stu-id="bf92c-155">The DeviceTopology API implements an [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface to represent the generic functions that are common to connectors and subunits.</span></span> <span data-ttu-id="bf92c-156">La API implementa las interfaces [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) y [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) para representar los aspectos específicos de los conectores y las subunidades.</span><span class="sxs-lookup"><span data-stu-id="bf92c-156">The API implements the [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) and [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) interfaces to represent the specific aspects of connectors and subunits.</span></span>

<span data-ttu-id="bf92c-157">La API de DeviceTopology construye las topologías del dispositivo de captura de onda y el dispositivo multiplexor de entrada desde los filtros de streaming de kernel (KS) que el controlador de audio expone al sistema operativo para representar estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bf92c-157">The DeviceTopology API constructs the topologies of the wave capture device and input multiplexer device from the kernel-streaming (KS) filters that the audio driver exposes to the operating system to represent these devices.</span></span> <span data-ttu-id="bf92c-158">(El controlador del adaptador de audio implementa las interfaces **IMiniportWaveXxx** y **IMiniportTopology** para representar las partes dependientes del hardware de estos filtros; para obtener más información acerca de estas interfaces y sobre los filtros KS, consulte la documentación del DDK de Windows).</span><span class="sxs-lookup"><span data-stu-id="bf92c-158">(The audio adapter driver implements **IMiniportWaveXxx** and **IMiniportTopology** interfaces to represent the hardware-dependent portions of these filters; for more information about these interfaces and about KS filters, see the Windows DDK documentation.)</span></span>

<span data-ttu-id="bf92c-159">La API de DeviceTopology crea topologías triviales para representar los dispositivos de punto de conexión A y B en el diagrama anterior.</span><span class="sxs-lookup"><span data-stu-id="bf92c-159">The DeviceTopology API constructs trivial topologies to represent endpoint devices A and B in the preceding diagram.</span></span> <span data-ttu-id="bf92c-160">La topología de dispositivo de un dispositivo de punto de conexión consta de un único conector.</span><span class="sxs-lookup"><span data-stu-id="bf92c-160">The device topology of an endpoint device consists of a single connector.</span></span> <span data-ttu-id="bf92c-161">Esta topología es simplemente un marcador de posición para el dispositivo de punto de conexión y no contiene subunidades para procesar datos de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-161">This topology is merely a placeholder for the endpoint device and contains no subunits for processing audio data.</span></span> <span data-ttu-id="bf92c-162">De hecho, los dispositivos de adaptador contienen todas las subunidades que las aplicaciones cliente utilizan para controlar el procesamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-162">In fact, adapter devices contain all of the subunits that client applications use to control audio processing.</span></span> <span data-ttu-id="bf92c-163">La topología de dispositivo de un dispositivo de punto de conexión sirve principalmente como punto de partida para explorar las topologías de dispositivos de los dispositivos de adaptador.</span><span class="sxs-lookup"><span data-stu-id="bf92c-163">The device topology of an endpoint device serves primarily as a starting point for exploring the device topologies of adapter devices.</span></span>

<span data-ttu-id="bf92c-164">Las conexiones internas entre dos partes de una topología de dispositivo se denominan vínculos.</span><span class="sxs-lookup"><span data-stu-id="bf92c-164">Internal connections between two parts in a device topology are called links.</span></span> <span data-ttu-id="bf92c-165">La API DeviceTopology proporciona métodos para atravesar vínculos de una parte a la siguiente en una topología de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-165">The DeviceTopology API provides methods for traversing links from one part to the next in a device topology.</span></span> <span data-ttu-id="bf92c-166">La API también proporciona métodos para atravesar las conexiones entre topologías de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bf92c-166">The API also provides methods for traversing the connections between device topologies.</span></span>

<span data-ttu-id="bf92c-167">Para comenzar la exploración de un conjunto de topologías de dispositivo conectado, una aplicación cliente activa la interfaz **IDeviceTopology** de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-167">To begin exploration of a set of connected device topologies, a client application activates the **IDeviceTopology** interface of an audio endpoint device.</span></span> <span data-ttu-id="bf92c-168">El conector de un dispositivo de extremo se conecta a un conector en un adaptador de audio o en una red.</span><span class="sxs-lookup"><span data-stu-id="bf92c-168">The connector in an endpoint device connects either to a connector in an audio adapter or to a network.</span></span> <span data-ttu-id="bf92c-169">Si el extremo se conecta a un dispositivo en un adaptador de audio, los métodos de la API de DeviceTopology permiten a la aplicación recorrer la conexión desde el extremo al adaptador obteniendo una referencia a la interfaz **IDeviceTopology** del dispositivo adaptador en el otro lado de la conexión.</span><span class="sxs-lookup"><span data-stu-id="bf92c-169">If the endpoint connects to a device on an audio adapter, then the methods in the DeviceTopology API enable the application to step across the connection from the endpoint to the adapter by obtaining a reference to the **IDeviceTopology** interface of the adapter device on the other side of the connection.</span></span> <span data-ttu-id="bf92c-170">Por otro lado, una red no tiene ninguna topología de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-170">A network, on the other hand, has no device topology.</span></span> <span data-ttu-id="bf92c-171">Una conexión de red canaliza una secuencia de audio a un cliente que tiene acceso al sistema de forma remota.</span><span class="sxs-lookup"><span data-stu-id="bf92c-171">A network connection pipes an audio stream to a client that is accessing the system remotely.</span></span>

<span data-ttu-id="bf92c-172">La API DeviceTopology proporciona acceso únicamente a las topologías de los dispositivos de hardware en un adaptador de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-172">The DeviceTopology API provides access only to the topologies of the hardware devices in an audio adapter.</span></span> <span data-ttu-id="bf92c-173">Los dispositivos externos en el borde izquierdo del diagrama y los componentes de software del borde derecho quedan fuera del ámbito de la API.</span><span class="sxs-lookup"><span data-stu-id="bf92c-173">The external devices on the left edge of the diagram and the software components on the right edge are beyond the scope of the API.</span></span> <span data-ttu-id="bf92c-174">Las líneas discontinuas de cada lado del diagrama representan los límites de la API de DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="bf92c-174">The dashed lines on either side of the diagram represent the limits of the DeviceTopology API.</span></span> <span data-ttu-id="bf92c-175">El cliente puede usar la API para explorar una ruta de acceso de datos que se estira del conector de entrada al bus del sistema, pero la API no puede penetrar más allá de estos límites.</span><span class="sxs-lookup"><span data-stu-id="bf92c-175">The client can use the API to explore a data path that stretches from the input jack to the system bus, but the API cannot penetrate beyond these boundaries.</span></span>

<span data-ttu-id="bf92c-176">Cada conector del diagrama anterior tiene asociado un tipo de conexión que indica el tipo de conexión que realiza el conector.</span><span class="sxs-lookup"><span data-stu-id="bf92c-176">Each connector in the preceding diagram has an associated connection type that indicates the type of connection that the connector makes.</span></span> <span data-ttu-id="bf92c-177">Por lo tanto, los conectores de los dos lados de una conexión siempre tienen tipos de conexión idénticos.</span><span class="sxs-lookup"><span data-stu-id="bf92c-177">Thus, the connectors on the two sides of a connection always have identical connection types.</span></span> <span data-ttu-id="bf92c-178">El tipo de conexión se indica mediante un valor de enumeración [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) ( \_ externa física, \_ interna física, software \_ fijo, \_ e/s de software o red).</span><span class="sxs-lookup"><span data-stu-id="bf92c-178">The connection type is indicated by a [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) enumeration value—Physical\_External, Physical\_Internal, Software\_Fixed, Software\_IO, or Network.</span></span> <span data-ttu-id="bf92c-179">Las conexiones entre el dispositivo de multiplexor de entrada y los dispositivos de punto de conexión A y B son del tipo \_ externo físico, lo que significa que la conexión representa una conexión física a un dispositivo externo (es decir, un conector de audio accesible desde el usuario).</span><span class="sxs-lookup"><span data-stu-id="bf92c-179">The connections between the input multiplexer device and endpoint devices A and B are of type Physical\_External, which means that the connection represents a physical connection to an external device (in other words, a user-accessible audio jack).</span></span> <span data-ttu-id="bf92c-180">La conexión a la señal analógica del reproductor de CD interno es del tipo \_ interno físico, que indica una conexión física a un dispositivo auxiliar que se instala dentro del chasis del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf92c-180">The connection to the analog signal from the internal CD player is of type Physical\_Internal, which indicates a physical connection to an auxiliary device that is installed inside the system chassis.</span></span> <span data-ttu-id="bf92c-181">La conexión entre el dispositivo de captura de onda y el dispositivo multiplexor de entrada es de tipo software \_ fijo, que indica una conexión permanente que se ha corregido y no se puede configurar en el control de software.</span><span class="sxs-lookup"><span data-stu-id="bf92c-181">The connection between the wave capture device and input multiplexer device is of type Software\_Fixed, which indicates a permanent connection that is fixed and cannot be configured under software control.</span></span> <span data-ttu-id="bf92c-182">Por último, la conexión al bus del sistema en el lado derecho del diagrama es de tipo e/s de software \_ , que indica que un motor DMA implementa la e/s de datos para la conexión en el control de software.</span><span class="sxs-lookup"><span data-stu-id="bf92c-182">Finally, the connection to the system bus on the right side of the diagram is of type Software\_IO, which indicates that the data I/O for the connection is implemented by a DMA engine under software control.</span></span> <span data-ttu-id="bf92c-183">(El diagrama no incluye un ejemplo de un tipo de conexión de red).</span><span class="sxs-lookup"><span data-stu-id="bf92c-183">(The diagram does not include an example of a Network connection type.)</span></span>

<span data-ttu-id="bf92c-184">El cliente comienza a atravesar una ruta de acceso de datos en el dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-184">The client begins traversing a data path at the endpoint device.</span></span> <span data-ttu-id="bf92c-185">En primer lugar, el cliente obtiene una interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa el dispositivo de punto de conexión, como se explica en [enumerar dispositivos de audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="bf92c-185">First, the client obtains an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface that represents the endpoint device, as explained in [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span> <span data-ttu-id="bf92c-186">Para obtener la interfaz **IDeviceTopology** para el dispositivo de extremo, el cliente llama al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el *IID* de parámetro establecido en REFIID IID \_ IDeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="bf92c-186">To obtain the **IDeviceTopology** interface for the endpoint device, the client calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to REFIID IID\_IDeviceTopology.</span></span>

<span data-ttu-id="bf92c-187">En el ejemplo del diagrama anterior, el dispositivo multiplexor de entrada contiene todos los controles de hardware (volumen, silencio y multiplexor) de las secuencias de captura de los conectores de entrada de línea y micrófono.</span><span class="sxs-lookup"><span data-stu-id="bf92c-187">In the example in the preceding diagram, the input multiplexer device contains all the hardware controls (volume, mute, and multiplexer) for the capture streams from the line-input and microphone jacks.</span></span> <span data-ttu-id="bf92c-188">En el ejemplo de código siguiente se muestra cómo obtener la interfaz **IDeviceTopology** para el dispositivo multiplexor de entrada desde la interfaz **IMMDevice** para el dispositivo de extremo para la entrada de línea o el micrófono:</span><span class="sxs-lookup"><span data-stu-id="bf92c-188">The following code example shows how to obtain the **IDeviceTopology** interface for the input multiplexer device from the **IMMDevice** interface for the endpoint device for the line input or microphone:</span></span>


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



<span data-ttu-id="bf92c-189">En la función GetHardwareDeviceTopology del ejemplo de código anterior se realizan los pasos siguientes para obtener la interfaz **IDeviceTopology** para el dispositivo multiplexor de entrada:</span><span class="sxs-lookup"><span data-stu-id="bf92c-189">The GetHardwareDeviceTopology function in the previous code example performs the following steps to obtain the **IDeviceTopology** interface for the input multiplexer device:</span></span>

1.  <span data-ttu-id="bf92c-190">Llame al método **IMMDevice:: Activate** para obtener la interfaz **IDeviceTopology** para el dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-190">Call the **IMMDevice::Activate** method to get the **IDeviceTopology** interface for the endpoint device.</span></span>
2.  <span data-ttu-id="bf92c-191">Con la interfaz **IDeviceTopology** obtenida en el paso anterior, llame al método [**IDeviceTopology:: GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) para obtener la interfaz **IConnector** del conector único (número de conector 0) en el dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-191">With the **IDeviceTopology** interface obtained in the preceding step, call the [**IDeviceTopology::GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) method to get the **IConnector** interface of the single connector (connector number 0) in the endpoint device.</span></span>
3.  <span data-ttu-id="bf92c-192">Con la interfaz **IConnector** obtenida en el paso anterior, llame al método [**IConnector:: GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) para obtener la interfaz **IConnector** del conector en el dispositivo multiplexor de entrada.</span><span class="sxs-lookup"><span data-stu-id="bf92c-192">With the **IConnector** interface obtained in the preceding step, call the [**IConnector::GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) method to get the **IConnector** interface of the connector in the input multiplexer device.</span></span>
4.  <span data-ttu-id="bf92c-193">Consulte la interfaz **IConnector** obtenida en el paso anterior para su interfaz **IPart** .</span><span class="sxs-lookup"><span data-stu-id="bf92c-193">Query the **IConnector** interface obtained in the preceding step for its **IPart** interface.</span></span>
5.  <span data-ttu-id="bf92c-194">Con la interfaz **IPart** obtenida en el paso anterior, llame al método [**IPart:: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) para obtener la interfaz **IDeviceTopology** para el dispositivo multiplexor de entrada.</span><span class="sxs-lookup"><span data-stu-id="bf92c-194">With the **IPart** interface obtained in the preceding step, call the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method to get the **IDeviceTopology** interface for the input multiplexer device.</span></span>

<span data-ttu-id="bf92c-195">Antes de que el usuario pueda grabar desde el micrófono en el diagrama anterior, la aplicación cliente debe asegurarse de que el multiplexor selecciona la entrada del micrófono.</span><span class="sxs-lookup"><span data-stu-id="bf92c-195">Before the user can record from the microphone in the preceding diagram, the client application must make certain that the multiplexer selects the microphone input.</span></span> <span data-ttu-id="bf92c-196">En el ejemplo de código siguiente se muestra cómo un cliente puede atravesar la ruta de acceso de datos del micrófono hasta que encuentra el multiplexor, que después programa para seleccionar la entrada del micrófono:</span><span class="sxs-lookup"><span data-stu-id="bf92c-196">The following code example shows how a client can traverse the data path from the microphone until it finds the multiplexer, which it then programs to select the microphone input:</span></span>


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



<span data-ttu-id="bf92c-197">La API de DeviceTopology implementa una interfaz [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) para encapsular un multiplexor, como el del diagrama anterior.</span><span class="sxs-lookup"><span data-stu-id="bf92c-197">The DeviceTopology API implements an [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) interface to encapsulate a multiplexer, such as the one in the preceding diagram.</span></span> <span data-ttu-id="bf92c-198">(Una interfaz [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) encapsula un demultiplexador). En el ejemplo de código anterior, el bucle interno de la función SelectCaptureDevice consulta cada subunidad que encuentra para detectar si la subunidad es un multiplexor.</span><span class="sxs-lookup"><span data-stu-id="bf92c-198">(An [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) interface encapsulates a demultiplexer.) In the preceding code example, the inner loop of the SelectCaptureDevice function queries each subunit that it finds to discover whether the subunit is a multiplexer.</span></span> <span data-ttu-id="bf92c-199">Si la subunidad es un multiplexor, la función llama al método [**IAudioInputSelector:: SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) para seleccionar la entrada que se conecta a la secuencia desde el dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-199">If the subunit is a multiplexer, then the function calls the [**IAudioInputSelector::SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) method to select the input that connects to the stream from the endpoint device.</span></span>

<span data-ttu-id="bf92c-200">En el ejemplo de código anterior, cada iteración del bucle exterior atraviesa una topología de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-200">In the preceding code example, each iteration of the outer loop traverses one device topology.</span></span> <span data-ttu-id="bf92c-201">Al atravesar las topologías del dispositivo en el diagrama anterior, la primera iteración atraviesa el dispositivo multiplexor de entrada y la segunda iteración atraviesa el dispositivo de captura de onda.</span><span class="sxs-lookup"><span data-stu-id="bf92c-201">When traversing the device topologies in the preceding diagram, the first iteration traverses the input multiplexer device and the second iteration traverses the wave capture device.</span></span> <span data-ttu-id="bf92c-202">La función terminará cuando llegue al conector en el borde derecho del diagrama.</span><span class="sxs-lookup"><span data-stu-id="bf92c-202">The function will terminate when it reaches the connector at the right edge of the diagram.</span></span> <span data-ttu-id="bf92c-203">La terminación se produce cuando la función detecta un conector con un \_ tipo de conexión de e/s de software.</span><span class="sxs-lookup"><span data-stu-id="bf92c-203">Termination occurs when the function detects a connector with a Software\_IO connection type.</span></span> <span data-ttu-id="bf92c-204">Este tipo de conexión identifica el punto en el que el dispositivo de adaptador se conecta al bus de sistema.</span><span class="sxs-lookup"><span data-stu-id="bf92c-204">This connection type identifies the point at which the adapter device connects to the system bus.</span></span>

<span data-ttu-id="bf92c-205">La llamada al método [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) en el ejemplo de código anterior obtiene un valor de enumeración **IPartType** que indica si la parte actual es un conector o una subunidad de procesamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="bf92c-205">The call to the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) method in the preceding code example obtains an **IPartType** enumeration value that indicates whether the current part is a connector or an audio-processing subunit.</span></span>

<span data-ttu-id="bf92c-206">El bucle interno en el ejemplo de código anterior recorre el vínculo de una parte a la siguiente llamando al método [**IPart:: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) .</span><span class="sxs-lookup"><span data-stu-id="bf92c-206">The inner loop in the preceding code example steps across the link from one part to the next by calling the [**IPart::EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) method.</span></span> <span data-ttu-id="bf92c-207">(También hay un método [**IPart:: EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) para la ejecución paso a paso en la dirección opuesta). Este método recupera un objeto [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) que contiene una lista de todos los elementos salientes.</span><span class="sxs-lookup"><span data-stu-id="bf92c-207">(There's also an [**IPart::EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) method for stepping in the opposite direction.) This method retrieves an [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) object that contains a list of all the outgoing parts.</span></span> <span data-ttu-id="bf92c-208">Sin embargo, cualquier parte que la función SelectCaptureDevice espera encontrar en un dispositivo de captura siempre tendrá exactamente un elemento saliente.</span><span class="sxs-lookup"><span data-stu-id="bf92c-208">However, any part that the SelectCaptureDevice function expects to encounter in a capture device will always have exactly one outgoing part.</span></span> <span data-ttu-id="bf92c-209">Por lo tanto, la siguiente llamada a [**IPartsList:: getPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) siempre solicita la primera parte de la lista, el número de parte 0, porque la función supone que se trata de la única parte de la lista.</span><span class="sxs-lookup"><span data-stu-id="bf92c-209">Thus, the subsequent call to [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) always requests the first part in the list, part number 0, because the function assumes that this is the only part in the list.</span></span>

<span data-ttu-id="bf92c-210">Si la función SelectCaptureDevice encuentra una topología para la que esa suposición no es válida, es posible que la función no pueda configurar correctamente el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf92c-210">If the SelectCaptureDevice function encounters a topology for which that assumption is not valid, the function might fail to configure the device correctly.</span></span> <span data-ttu-id="bf92c-211">Para evitar este tipo de error, una versión más general de la función podría hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf92c-211">To avoid such a failure, a more general-purpose version of the function might do the following:</span></span>

-   <span data-ttu-id="bf92c-212">Llame al método [**IPartsList:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) para determinar el número de elementos salientes.</span><span class="sxs-lookup"><span data-stu-id="bf92c-212">Call the [**IPartsList::GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) method to determine the number of outgoing parts.</span></span>
-   <span data-ttu-id="bf92c-213">Para cada elemento saliente, llame a **IPartsList:: getPart** para empezar a atravesar la ruta de acceso de datos que conduce desde la parte.</span><span class="sxs-lookup"><span data-stu-id="bf92c-213">For each outgoing part, call **IPartsList::GetPart** to begin to traverse the data path that leads from the part.</span></span>

<span data-ttu-id="bf92c-214">Algunos de los elementos, pero no necesariamente todos, tienen controles de hardware asociados que los clientes pueden establecer u obtener.</span><span class="sxs-lookup"><span data-stu-id="bf92c-214">Some, but not necessarily all, parts have associated hardware controls that clients can set or get.</span></span> <span data-ttu-id="bf92c-215">Una parte determinada puede tener cero, uno o más controles de hardware.</span><span class="sxs-lookup"><span data-stu-id="bf92c-215">A particular part might have zero, one, or more hardware controls.</span></span> <span data-ttu-id="bf92c-216">Un control de hardware se representa mediante el siguiente par de interfaces:</span><span class="sxs-lookup"><span data-stu-id="bf92c-216">A hardware control is represented by the following pair of interfaces:</span></span>

-   <span data-ttu-id="bf92c-217">Una interfaz de control genérico, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), que tiene métodos comunes a todos los controles de hardware.</span><span class="sxs-lookup"><span data-stu-id="bf92c-217">A generic control interface, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), which has methods that are common to all hardware controls.</span></span>
-   <span data-ttu-id="bf92c-218">Una interfaz específica de la función (por ejemplo, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) que expone los parámetros de control para un tipo determinado de control de hardware (por ejemplo, un control de volumen).</span><span class="sxs-lookup"><span data-stu-id="bf92c-218">A function-specific interface (for example, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) that exposes the control parameters for a particular type of hardware control (for example, a volume control).</span></span>

<span data-ttu-id="bf92c-219">Para enumerar los controles de hardware de un elemento, el cliente llama primero al método [**IPart:: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) para determinar el número de controles de hardware que están asociados a la parte.</span><span class="sxs-lookup"><span data-stu-id="bf92c-219">To enumerate the hardware controls for a part, the client first calls the [**IPart::GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) method to determine the number of hardware controls that are associated with the part.</span></span> <span data-ttu-id="bf92c-220">Después, el cliente realiza una serie de llamadas al método [**IPart:: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) para obtener la interfaz **IControlInterface** para cada control de hardware.</span><span class="sxs-lookup"><span data-stu-id="bf92c-220">Next, the client makes a series of calls to the [**IPart::GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) method to obtain the **IControlInterface** interface for each hardware control.</span></span> <span data-ttu-id="bf92c-221">Por último, el cliente obtiene la interfaz específica de la función para cada control de hardware llamando al método [**IControlInterface:: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) para obtener el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="bf92c-221">Finally, the client obtains the function-specific interface for each hardware control by calling the [**IControlInterface::GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) method to obtain the interface ID.</span></span> <span data-ttu-id="bf92c-222">El cliente llama al método [**IPart:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) con este identificador para obtener la interfaz específica de la función.</span><span class="sxs-lookup"><span data-stu-id="bf92c-222">The client calls the [**IPart::Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) method with this ID to obtain the function-specific interface.</span></span>

<span data-ttu-id="bf92c-223">Una parte que es un conector podría admitir una de las siguientes interfaces de control específicas de la función:</span><span class="sxs-lookup"><span data-stu-id="bf92c-223">A part that is a connector might support one of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="bf92c-224">**IKsFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="bf92c-224">**IKsFormatSupport**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [<span data-ttu-id="bf92c-225">**IKsJackDescription**</span><span class="sxs-lookup"><span data-stu-id="bf92c-225">**IKsJackDescription**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

<span data-ttu-id="bf92c-226">Una parte que es una subunidad podría admitir una o varias de las siguientes interfaces de control específicas de la función:</span><span class="sxs-lookup"><span data-stu-id="bf92c-226">A part that is a subunit might support one or more of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="bf92c-227">**IAudioAutoGainControl**</span><span class="sxs-lookup"><span data-stu-id="bf92c-227">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [<span data-ttu-id="bf92c-228">**IAudioBass**</span><span class="sxs-lookup"><span data-stu-id="bf92c-228">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [<span data-ttu-id="bf92c-229">**IAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="bf92c-229">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [<span data-ttu-id="bf92c-230">**IAudioInputSelector**</span><span class="sxs-lookup"><span data-stu-id="bf92c-230">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [<span data-ttu-id="bf92c-231">**IAudioLoudness**</span><span class="sxs-lookup"><span data-stu-id="bf92c-231">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [<span data-ttu-id="bf92c-232">**IAudioMidrange**</span><span class="sxs-lookup"><span data-stu-id="bf92c-232">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [<span data-ttu-id="bf92c-233">**IAudioMute**</span><span class="sxs-lookup"><span data-stu-id="bf92c-233">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [<span data-ttu-id="bf92c-234">**IAudioOutputSelector**</span><span class="sxs-lookup"><span data-stu-id="bf92c-234">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [<span data-ttu-id="bf92c-235">**IAudioPeakMeter**</span><span class="sxs-lookup"><span data-stu-id="bf92c-235">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [<span data-ttu-id="bf92c-236">**IAudioTreble**</span><span class="sxs-lookup"><span data-stu-id="bf92c-236">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [<span data-ttu-id="bf92c-237">**IAudioVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="bf92c-237">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [<span data-ttu-id="bf92c-238">**IDeviceSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="bf92c-238">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

<span data-ttu-id="bf92c-239">Un elemento admite la interfaz **IDeviceSpecificProperty** solo si el control de hardware subyacente tiene un valor de control específico del dispositivo y el control no se puede representar de forma adecuada con ninguna otra interfaz específica de la función de la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="bf92c-239">A part supports the **IDeviceSpecificProperty** interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other function-specific interface in the preceding list.</span></span> <span data-ttu-id="bf92c-240">Normalmente, una propiedad específica del dispositivo solo es útil para un cliente que puede inferir el significado del valor de propiedad a partir de información como el tipo de elemento, el subtipo de elemento y el nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="bf92c-240">Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name.</span></span> <span data-ttu-id="bf92c-241">El cliente puede obtener esta información mediante una llamada a los métodos [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)y [**IPart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .</span><span class="sxs-lookup"><span data-stu-id="bf92c-241">The client can obtain this information by calling the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype), and [**IPart::GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf92c-242">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf92c-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf92c-243">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="bf92c-243">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
