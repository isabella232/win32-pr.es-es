---
description: Si el host y el cliente genéricos se pueden ver entre sí en la red, pero el host y el cliente reales no pueden, es probable que el problema esté en los mensajes enviados entre los puntos de conexión a través de la red.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Usar el cliente de depuración WSD para comprobar el tráfico de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f03e06baefc40bad843a5193b2cec604383251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716125"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="66af6-103">Usar el cliente de depuración WSD para comprobar el tráfico de multidifusión</span><span class="sxs-lookup"><span data-stu-id="66af6-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="66af6-104">Si el host y el cliente genéricos se pueden ver entre sí en la red, pero el host y el cliente reales no pueden, es probable que el problema esté en los mensajes enviados entre los puntos de conexión a través de la red.</span><span class="sxs-lookup"><span data-stu-id="66af6-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="66af6-105">Para obtener más información sobre el host y el cliente genéricos, vea [usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="66af6-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="66af6-106">Dado que los seguimientos de red completos pueden ser difíciles de recopilar, filtrar y leer, la herramienta cliente de depuración WSD se puede usar para imprimir los lados de la multidifusión de los mensajes de WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="66af6-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="66af6-107">El cliente de depuración de WSD en modo de multidifusión solo puede inspeccionar la mitad de los mensajes, ya que el cliente no puede imprimir mensajes de unidifusión.</span><span class="sxs-lookup"><span data-stu-id="66af6-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="66af6-108">Si el tráfico de unidifusión es de interés, vaya directamente a [inspeccionar los seguimientos de red para el WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="66af6-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="66af6-109">Este procedimiento muestra un método que mostrará todo el tráfico de multidifusión de la red.</span><span class="sxs-lookup"><span data-stu-id="66af6-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="66af6-110">Para mostrar solo el tráfico de multidifusión hacia y desde el dispositivo, consulte la sección filtrado de los [resultados del cliente de depuración WSD](#filtering-wsd-debug-client-results) más adelante.</span><span class="sxs-lookup"><span data-stu-id="66af6-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="66af6-111">**Para usar el cliente de depuración WSD para comprobar el tráfico de multidifusión**</span><span class="sxs-lookup"><span data-stu-id="66af6-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="66af6-112">Configure el host y el cliente para que se ejecuten en la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).</span><span class="sxs-lookup"><span data-stu-id="66af6-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="66af6-113">Abra un símbolo del sistema y ejecute el comando siguiente: **WSDDebug \_client.exe/Mode multidifusión**</span><span class="sxs-lookup"><span data-stu-id="66af6-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="66af6-114">Reproduzca el error iniciando el host y el cliente, o presionando F5 en el explorador de red.</span><span class="sxs-lookup"><span data-stu-id="66af6-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="66af6-115">Compruebe que los mensajes se están multidifusión.</span><span class="sxs-lookup"><span data-stu-id="66af6-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="66af6-116">Si los mensajes necesarios se muestran en la salida del cliente de depuración de WSD, el error de la aplicación puede estar en el contenido del mensaje de multidifusión o en la existencia o el contenido de los mensajes de respuesta de unidifusión correspondientes.</span><span class="sxs-lookup"><span data-stu-id="66af6-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="66af6-117">Siga las instrucciones que se indican en [inspeccionar seguimientos de red para UDP WS-Discovery para](inspecting-network-traces-for-udp-ws-discovery.md)continuar con la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="66af6-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="66af6-118">Si los mensajes necesarios se muestran en la salida del cliente de depuración de WSD, es probable que se haya identificado el origen del problema de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66af6-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="66af6-119">Es probable que el tráfico de multidifusión no se transmita a la red.</span><span class="sxs-lookup"><span data-stu-id="66af6-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="66af6-120">Este error puede producirse cuando la aplicación no enumera correctamente los adaptadores de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="66af6-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="66af6-121">Las aplicaciones deben enviar explícitamente tráfico de multidifusión a través de todas las interfaces de red. de lo contrario, es posible que no se generen paquetes para la interfaz de bucle invertido ni para otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="66af6-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="66af6-122">Para comprobar que los paquetes no aparecen en la red, siga las instrucciones de inspección de los [seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md) y busque la evidencia de mensajes de multidifusión que faltan.</span><span class="sxs-lookup"><span data-stu-id="66af6-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="66af6-123">Comprobando que los mensajes se están multidifusión</span><span class="sxs-lookup"><span data-stu-id="66af6-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="66af6-124">Compruebe siempre que los mensajes de [sondeo](probe-message.md) sean de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="66af6-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="66af6-125">Opcionalmente, compruebe que los mensajes [Hello](hello-message.md) y [Resolve](resolve-message.md) se están multidifusión.</span><span class="sxs-lookup"><span data-stu-id="66af6-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="66af6-126">Tenga en cuenta que no todas las aplicaciones usan mensajes de resolución.</span><span class="sxs-lookup"><span data-stu-id="66af6-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="66af6-127">Para obtener más información acerca de los patrones de mensaje que usan los clientes y los hosts, consulte [patrones de mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md) y [Introducción con WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="66af6-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="66af6-128">Los mensajes se deben desencadenar para enviarlos como se describe en el paso 3 anterior.</span><span class="sxs-lookup"><span data-stu-id="66af6-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="66af6-129">El cliente de depuración de WSD muestra el mensaje SOAP sin formato como salida.</span><span class="sxs-lookup"><span data-stu-id="66af6-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="66af6-130">Dado que todos los mensajes impresos por el cliente de depuración de WSD en modo de multidifusión se reciben a través de un socket de multidifusión, no se muestra la dirección de destino del mensaje.</span><span class="sxs-lookup"><span data-stu-id="66af6-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="66af6-131">El siguiente ejemplo de salida de cliente de depuración WSD muestra un mensaje de sondeo.</span><span class="sxs-lookup"><span data-stu-id="66af6-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="66af6-132">El elemento <WSA: Action> identifica el mensaje como un mensaje de sondeo.</span><span class="sxs-lookup"><span data-stu-id="66af6-132">The <wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="66af6-133">Inspeccione el campo <WSA: Action> para comprobar que el mensaje recibido era un mensaje de sondeo.</span><span class="sxs-lookup"><span data-stu-id="66af6-133">Inspect the <wsa:Action> field to verify that the received message was a Probe message.</span></span>

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

<span data-ttu-id="66af6-134">El siguiente ejemplo de salida de cliente de depuración WSD muestra un mensaje de saludo.</span><span class="sxs-lookup"><span data-stu-id="66af6-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="66af6-135">El elemento <WSA: Action> identifica el mensaje como un mensaje de saludo.</span><span class="sxs-lookup"><span data-stu-id="66af6-135">The <wsa:Action> element identifies the message as a Hello message.</span></span>

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="66af6-136">Filtrar resultados del cliente de depuración WSD</span><span class="sxs-lookup"><span data-stu-id="66af6-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="66af6-137">El filtrado de los resultados del cliente de depuración WSD puede ayudar a identificar el tráfico de incidentes relacionado con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66af6-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="66af6-138">El filtrado solo es necesario en redes ruidosos.</span><span class="sxs-lookup"><span data-stu-id="66af6-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="66af6-139">Hay dos formas de filtrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="66af6-139">There are two ways to filter results.</span></span> <span data-ttu-id="66af6-140">Las direcciones IP que se van a filtrar se pueden identificar explícitamente al iniciar el cliente de depuración de WSD.</span><span class="sxs-lookup"><span data-stu-id="66af6-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="66af6-141">Como alternativa, se pueden especificar las direcciones IP una vez iniciado el cliente.</span><span class="sxs-lookup"><span data-stu-id="66af6-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="66af6-142">En esta sección se describen ambos métodos.</span><span class="sxs-lookup"><span data-stu-id="66af6-142">This section describes both methods.</span></span>

<span data-ttu-id="66af6-143">**Para especificar las direcciones IP que se van a filtrar al iniciar el cliente de depuración WSD**</span><span class="sxs-lookup"><span data-stu-id="66af6-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="66af6-144">Configure el host y el cliente para que se ejecuten en la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).</span><span class="sxs-lookup"><span data-stu-id="66af6-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="66af6-145">Recopilar las direcciones IP del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66af6-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="66af6-146">Si el dispositivo tiene varias direcciones (por ejemplo, tiene direcciones IPv4 e IPv6), se deben recopilar todas las direcciones.</span><span class="sxs-lookup"><span data-stu-id="66af6-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="66af6-147">Abra un símbolo del sistema y ejecute el comando siguiente: \**WSDDebug \_client.exe/Mode multicast/IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="66af6-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="66af6-148">*<device IP>* es una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="66af6-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="66af6-149">En la lista siguiente se muestran algunos formatos de ejemplo para esta dirección IP.</span><span class="sxs-lookup"><span data-stu-id="66af6-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="66af6-150">192.168.0.1</span><span class="sxs-lookup"><span data-stu-id="66af6-150">192.168.0.1</span></span>
-   <span data-ttu-id="66af6-151">:: 1</span><span class="sxs-lookup"><span data-stu-id="66af6-151">::1</span></span>
-   <span data-ttu-id="66af6-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="66af6-152">mydevice.contoso.com</span></span>

<span data-ttu-id="66af6-153">El cliente de depuración de WSD resuelve automáticamente los nombres de host proporcionados en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="66af6-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="66af6-154">**Para filtrar los resultados después de iniciar el cliente de depuración de WSD**</span><span class="sxs-lookup"><span data-stu-id="66af6-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="66af6-155">Configure el host y el cliente para que se ejecuten en la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).</span><span class="sxs-lookup"><span data-stu-id="66af6-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="66af6-156">Recopilar las direcciones IP del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66af6-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="66af6-157">Si el dispositivo tiene varias direcciones (por ejemplo, tiene direcciones IPv4 e IPv6), se deben recopilar todas las direcciones.</span><span class="sxs-lookup"><span data-stu-id="66af6-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="66af6-158">Abra un símbolo del sistema y ejecute el comando siguiente: **WSDDebug \_client.exe/Mode multidifusión**</span><span class="sxs-lookup"><span data-stu-id="66af6-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="66af6-159">En el símbolo del sistema del cliente de depuración WSD, ejecute el siguiente comando: \**IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="66af6-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="66af6-160">Repita el paso 4 hasta que se hayan agregado todas las direcciones IP del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66af6-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="66af6-161">En el procedimiento siguiente se da por supuesto que se ha iniciado el cliente de depuración WSD y que se está filtrando por dirección IP.</span><span class="sxs-lookup"><span data-stu-id="66af6-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="66af6-162">**Para comprobar que se están filtrando las direcciones IP correctas**</span><span class="sxs-lookup"><span data-stu-id="66af6-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="66af6-163">En el símbolo del sistema del cliente de depuración WSD, ejecute el siguiente comando: **IP Print**</span><span class="sxs-lookup"><span data-stu-id="66af6-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="66af6-164">Aparece la lista de direcciones IP que se filtran.</span><span class="sxs-lookup"><span data-stu-id="66af6-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="66af6-165">En el procedimiento siguiente se da por supuesto que se ha iniciado el cliente de depuración WSD y que se está filtrando por dirección IP.</span><span class="sxs-lookup"><span data-stu-id="66af6-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="66af6-166">**Para deshabilitar el filtrado**</span><span class="sxs-lookup"><span data-stu-id="66af6-166">**To disable filtering**</span></span>

-   <span data-ttu-id="66af6-167">En el símbolo del sistema del cliente de depuración WSD, ejecute el siguiente comando: **IP Clear**</span><span class="sxs-lookup"><span data-stu-id="66af6-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="66af6-168">Ahora se mostrará todo el tráfico de multidifusión en la salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="66af6-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66af6-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66af6-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66af6-170">Procedimientos de diagnóstico de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="66af6-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="66af6-171">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="66af6-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



