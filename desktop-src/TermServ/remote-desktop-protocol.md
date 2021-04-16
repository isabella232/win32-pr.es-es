---
title: Protocolo de escritorio remoto
description: El protocolo de Escritorio remoto de Microsoft (RDP) proporciona funciones de entrada y visualización remotas a través de conexiones de red para aplicaciones basadas en Windows que se ejecutan en un servidor.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Protocolo de escritorio remoto (RDP) Servicios de Escritorio remoto
- RDP (consulte Protocolo de escritorio remoto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685734"
---
# <a name="remote-desktop-protocol"></a><span data-ttu-id="f0d64-105">Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="f0d64-105">Remote Desktop Protocol</span></span>

<span data-ttu-id="f0d64-106">El protocolo de Escritorio remoto de Microsoft (RDP) proporciona funciones de entrada y visualización remotas a través de conexiones de red para aplicaciones basadas en Windows que se ejecutan en un servidor.</span><span class="sxs-lookup"><span data-stu-id="f0d64-106">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span> <span data-ttu-id="f0d64-107">RDP está diseñado para admitir distintos tipos de topologías de red y varios protocolos de LAN.</span><span class="sxs-lookup"><span data-stu-id="f0d64-107">RDP is designed to support different types of network topologies and multiple LAN protocols.</span></span>

> [!Note]  
> <span data-ttu-id="f0d64-108">Este tema está destinado a los desarrolladores de software.</span><span class="sxs-lookup"><span data-stu-id="f0d64-108">This topic is for software developers.</span></span> <span data-ttu-id="f0d64-109">Si busca información de usuario para Escritorio remoto, consulte [soporte técnico de Windows](https://windows.microsoft.com/windows/support#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="f0d64-109">If you are looking for user information for Remote Desktop, see [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span></span> <span data-ttu-id="f0d64-110">Si está buscando información profesional de TI para Escritorio remoto, consulte [servicios de escritorio remoto en TechNet](/windows/deployment/deploy-whats-new).</span><span class="sxs-lookup"><span data-stu-id="f0d64-110">If you are looking for IT professional information for Remote Desktop, see [Remote Desktop Services on TechNet](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="basic-architecture"></a><span data-ttu-id="f0d64-111">Arquitectura básica</span><span class="sxs-lookup"><span data-stu-id="f0d64-111">Basic Architecture</span></span>

<span data-ttu-id="f0d64-112">RDP se basa en y en una extensión de la familia de protocolos ITU T. 120.</span><span class="sxs-lookup"><span data-stu-id="f0d64-112">RDP is based on, and an extension of, the ITU T.120 family of protocols.</span></span> <span data-ttu-id="f0d64-113">RDP es un protocolo compatible con varios canales que permite canales virtuales independientes para llevar la comunicación del dispositivo y los datos de presentación del servidor, así como datos del mouse y del teclado del cliente cifrados.</span><span class="sxs-lookup"><span data-stu-id="f0d64-113">RDP is a multiple-channel capable protocol that allows for separate virtual channels for carrying device communication and presentation data from the server, as well as encrypted client mouse and keyboard data.</span></span> <span data-ttu-id="f0d64-114">RDP proporciona una base extensible y admite hasta 64.000 canales independientes para la transmisión de datos y aprovisionaciones para la transmisión multipunto.</span><span class="sxs-lookup"><span data-stu-id="f0d64-114">RDP provides an extensible base and supports up to 64,000 separate channels for data transmission and provisions for multipoint transmission.</span></span>

<span data-ttu-id="f0d64-115">En el servidor, RDP usa su propio controlador de vídeo para representar la salida de la presentación mediante la creación de la información de representación en paquetes de red mediante el protocolo RDP y su envío a través de la red al cliente.</span><span class="sxs-lookup"><span data-stu-id="f0d64-115">On the server, RDP uses its own video driver to render display output by constructing the rendering information into network packets by using RDP protocol and sending them over the network to the client.</span></span> <span data-ttu-id="f0d64-116">En el cliente, RDP recibe datos de representación e interpreta los paquetes en las llamadas a la API de la interfaz de dispositivo gráfico (GDI) de Microsoft Windows correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f0d64-116">On the client, RDP receives rendering data and interprets the packets into corresponding Microsoft Windows graphics device interface (GDI) API calls.</span></span> <span data-ttu-id="f0d64-117">En la ruta de acceso de entrada, los eventos del mouse y del teclado del cliente se redirigen desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="f0d64-117">For the input path, client mouse and keyboard events are redirected from the client to the server.</span></span> <span data-ttu-id="f0d64-118">En el servidor, RDP usa su propio controlador de teclado y de mouse para recibir estos eventos de teclado y de mouse.</span><span class="sxs-lookup"><span data-stu-id="f0d64-118">On the server, RDP uses its own keyboard and mouse driver to receive these keyboard and mouse events.</span></span>

<span data-ttu-id="f0d64-119">En una sesión de Escritorio remoto, todas las variables de entorno (por ejemplo, las variables que determinan la profundidad de color y el fondo para habilitar y deshabilitar) se determinan mediante la configuración de conexión RCP-Tcp.</span><span class="sxs-lookup"><span data-stu-id="f0d64-119">In a Remote Desktop session, all environment variables—for example, variables determining color depth and wallpaper enabling and disabling—are determined by the RCP-Tcp connection settings.</span></span> <span data-ttu-id="f0d64-120">Esto se aplica a todas las funciones y métodos que establecen variables de entorno en la [conexión web a escritorio remoto referencia](remote-desktop-web-connection-reference.md) y la [interfaz del proveedor de WMI servicios de escritorio remoto](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f0d64-120">This applies to all functions and methods that set environment variables in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) and the [Remote Desktop Services WMI Provider interface](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="features"></a><span data-ttu-id="f0d64-121">Características</span><span class="sxs-lookup"><span data-stu-id="f0d64-121">Features</span></span>

<span data-ttu-id="f0d64-122">Microsoft RDP incluye las siguientes características y capacidades:</span><span class="sxs-lookup"><span data-stu-id="f0d64-122">Microsoft RDP includes the following features and capabilities:</span></span>

<dl> <dt>

<span data-ttu-id="f0d64-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Cifra</span><span class="sxs-lookup"><span data-stu-id="f0d64-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encryption</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-124">RDP usa el cifrado RC4 de seguridad de RSA, un cifrado de flujo diseñado para cifrar de forma eficaz cantidades pequeñas de datos.</span><span class="sxs-lookup"><span data-stu-id="f0d64-124">RDP uses RSA Security's RC4 cipher, a stream cipher designed to efficiently encrypt small amounts of data.</span></span> <span data-ttu-id="f0d64-125">RC4 está diseñado para comunicaciones seguras a través de redes.</span><span class="sxs-lookup"><span data-stu-id="f0d64-125">RC4 is designed for secure communications over networks.</span></span> <span data-ttu-id="f0d64-126">Los administradores pueden elegir cifrar los datos mediante una clave de 56 o 128 bits.</span><span class="sxs-lookup"><span data-stu-id="f0d64-126">Administrators can choose to encrypt data by using a 56- or 128-bit key.</span></span>

</dd> <dt>

<span data-ttu-id="f0d64-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Características de reducción de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="f0d64-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Bandwidth reduction features</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-128">RDP admite varios mecanismos para reducir la cantidad de datos transmitidos a través de una conexión de red.</span><span class="sxs-lookup"><span data-stu-id="f0d64-128">RDP supports various mechanisms to reduce the amount of data transmitted over a network connection.</span></span> <span data-ttu-id="f0d64-129">Los mecanismos incluyen la compresión de datos, el almacenamiento en caché persistente de mapas de bits y el almacenamiento en caché de glifos y fragmentos en la RAM.</span><span class="sxs-lookup"><span data-stu-id="f0d64-129">Mechanisms include data compression, persistent caching of bitmaps, and caching of glyphs and fragments in RAM.</span></span> <span data-ttu-id="f0d64-130">La caché de mapa de bits persistente puede proporcionar una mejora sustancial en el rendimiento de las conexiones de ancho de banda bajo, especialmente cuando se ejecutan aplicaciones que hacen un uso extensivo de mapas de bits grandes.</span><span class="sxs-lookup"><span data-stu-id="f0d64-130">The persistent bitmap cache can provide a substantial improvement in performance over low-bandwidth connections, especially when running applications that make extensive use of large bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="f0d64-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Desconexión de itinerancia</span><span class="sxs-lookup"><span data-stu-id="f0d64-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming disconnect</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-132">Un usuario puede desconectarse manualmente de una sesión de escritorio remoto sin cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="f0d64-132">A user can manually disconnect from a remote desktop session without logging off.</span></span> <span data-ttu-id="f0d64-133">El usuario se vuelve a conectar automáticamente a la sesión desconectada cuando vuelve a iniciar sesión en el sistema, ya sea desde el mismo dispositivo o desde otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0d64-133">The user is automatically reconnected to their disconnected session when he or she logs back onto the system, either from the same device or a different device.</span></span> <span data-ttu-id="f0d64-134">Cuando una sesión de usuario termina inesperadamente debido a un error de red o de cliente, el usuario se desconecta pero no se cierra.</span><span class="sxs-lookup"><span data-stu-id="f0d64-134">When a user's session is unexpectedly terminated by a network or client failure, the user is disconnected but not logged off.</span></span>

</dd> <dt>

<span data-ttu-id="f0d64-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Asignación del portapapeles</span><span class="sxs-lookup"><span data-stu-id="f0d64-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Clipboard mapping</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-136">Los usuarios pueden eliminar, copiar y pegar texto y gráficos entre aplicaciones que se ejecutan en el equipo local y que se ejecutan en una sesión de escritorio remoto, y entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="f0d64-136">Users can delete, copy, and paste text and graphics between applications running on the local computer and those running in a remote desktop session, and between sessions.</span></span>

</dd> <dt>

<span data-ttu-id="f0d64-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Redirección de impresión</span><span class="sxs-lookup"><span data-stu-id="f0d64-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Print redirection</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-138">Las aplicaciones que se ejecutan en una sesión de escritorio remoto pueden imprimir en una impresora conectada al dispositivo cliente.</span><span class="sxs-lookup"><span data-stu-id="f0d64-138">Applications running within a remote desktop session can print to a printer attached to the client device.</span></span>

</dd> <dt>

<span data-ttu-id="f0d64-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canales virtuales</span><span class="sxs-lookup"><span data-stu-id="f0d64-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtual channels</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-140">Mediante el uso de la arquitectura de canal virtual de RDP, se pueden aumentar las aplicaciones existentes y se pueden desarrollar nuevas aplicaciones para agregar características que requieran comunicaciones entre el dispositivo cliente y una aplicación que se ejecute en una sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f0d64-140">By using RDP virtual channel architecture, existing applications can be augmented and new applications can be developed to add features that require communications between the client device and an application running in a remote desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="f0d64-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Control remoto</span><span class="sxs-lookup"><span data-stu-id="f0d64-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote control</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-142">El personal de soporte técnico de equipos puede ver y controlar una sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f0d64-142">Computer support staff can view and control a remote desktop session.</span></span> <span data-ttu-id="f0d64-143">Compartir entradas y mostrar gráficos entre dos sesiones de escritorio remoto ofrece a una persona de soporte técnico la capacidad de diagnosticar y resolver problemas de forma remota.</span><span class="sxs-lookup"><span data-stu-id="f0d64-143">Sharing input and display graphics between two remote desktop sessions gives a support person the ability to diagnose and resolve problems remotely.</span></span>

</dd> <dt>

<span data-ttu-id="f0d64-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Equilibrio de carga de red</span><span class="sxs-lookup"><span data-stu-id="f0d64-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network load balancing</span></span>
</dt> <dd>

<span data-ttu-id="f0d64-145">RDP aprovecha el equilibrio de carga de red (NLB), si está disponible.</span><span class="sxs-lookup"><span data-stu-id="f0d64-145">RDP takes advantage of network load balancing (NLB), where available.</span></span>

</dd> </dl>

<span data-ttu-id="f0d64-146">Además, RDP contiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="f0d64-146">In addition, RDP contains the following features:</span></span>

-   <span data-ttu-id="f0d64-147">Compatibilidad con color de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="f0d64-147">Support for 24-bit color.</span></span>
-   <span data-ttu-id="f0d64-148">Rendimiento mejorado en conexiones de acceso telefónico de baja velocidad a través de un ancho de banda reducido.</span><span class="sxs-lookup"><span data-stu-id="f0d64-148">Improved performance over low-speed dial-up connections through reduced bandwidth.</span></span>
-   <span data-ttu-id="f0d64-149">Autenticación mediante tarjeta inteligente a través de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f0d64-149">Smart Card authentication through Remote Desktop Services.</span></span>
-   <span data-ttu-id="f0d64-150">Enlace de teclado.</span><span class="sxs-lookup"><span data-stu-id="f0d64-150">Keyboard hooking.</span></span> <span data-ttu-id="f0d64-151">La capacidad de dirigir combinaciones especiales de teclas de Windows, en modo de pantalla completa, al equipo local o a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="f0d64-151">The ability to direct special Windows key combinations, in full-screen mode, to the local computer or to a remote computer.</span></span>
-   <span data-ttu-id="f0d64-152">Redirección de sonido, unidad, puerto e impresora de red.</span><span class="sxs-lookup"><span data-stu-id="f0d64-152">Sound, drive, port, and network printer redirection.</span></span> <span data-ttu-id="f0d64-153">Los sonidos que se producen en el equipo remoto pueden escucharse en el equipo cliente que ejecuta el cliente RDC y las unidades de cliente locales estarán visibles para la sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f0d64-153">Sounds that occur on the remote computer can be heard on the client computer running the RDC client, and local client drives will be visible to the remote desktop session.</span></span>

 

 