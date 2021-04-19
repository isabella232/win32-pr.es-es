---
description: Si el host genérico y el cliente pueden verse entre sí en la red pero el host y el cliente reales no pueden, es probable que el problema esté en los mensajes enviados entre los puntos de conexión a través de la red.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Uso del cliente de depuración de WSD para comprobar el tráfico de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a814ac97512ef4b0691c22d3238d151372023a7
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380669"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>Uso del cliente de depuración de WSD para comprobar el tráfico de multidifusión

Si el host genérico y el cliente pueden verse entre sí en la red pero el host y el cliente reales no pueden, es probable que el problema esté en los mensajes enviados entre los puntos de conexión a través de la red. Para obtener más información sobre el host y el cliente genéricos, vea [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md). Dado que los seguimientos de red completos pueden ser difíciles de recopilar, filtrar y leer, se puede usar la herramienta cliente de depuración de WSD para imprimir los lados de multidifusión de WS-Discovery mensajes.

El cliente de depuración de WSD en modo de multidifusión solo puede inspeccionar la mitad de los mensajes, ya que el cliente no puede imprimir mensajes de unidifusión. Si el tráfico de unidifusión es de interés, vaya directamente a [Inspecting Network Traces for UDP WS-Discovery (Inspección de seguimientos de red para UDP WS-Discovery).](inspecting-network-traces-for-udp-ws-discovery.md)

Este procedimiento muestra un método que mostrará todo el tráfico de multidifusión en la red. Para mostrar solo el tráfico de multidifusión hacia y desde el dispositivo, consulte la sección Filtrado de los resultados del cliente de depuración de [WSD](#filtering-wsd-debug-client-results) a continuación.

**Para usar el cliente de depuración de WSD para comprobar el tráfico de multidifusión**

1.  Configure el host y el cliente para que se ejecuten a través de la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Abra un símbolo del sistema y ejecute el siguiente comando: **WSDDebug \_client.exe multidifusión /mode**
3.  Reproduzca el error iniciando el host y el cliente o presionando F5 en el Explorador de red.
4.  Compruebe que los mensajes se están multidifusión.

Si los mensajes necesarios se muestran en la salida del cliente de depuración de WSD, el error de la aplicación puede estar en el contenido del mensaje de multidifusión o en la existencia o el contenido de los mensajes de respuesta de unidifusión correspondientes. Para continuar con la solución de problemas, siga las instrucciones de [Inspección de seguimientos de red para UDP WS-Discovery.](inspecting-network-traces-for-udp-ws-discovery.md)

Si los mensajes necesarios se muestran en la salida del cliente de depuración de WSD, es probable que se haya identificado el origen del problema de la aplicación. Es probable que el tráfico de multidifusión no se transmita en la red. Este error puede producirse cuando la aplicación no enumera correctamente los adaptadores de multidifusión. Las aplicaciones deben enviar explícitamente tráfico de multidifusión a través de todas las interfaces de red; De lo contrario, es posible que no se generen paquetes para la interfaz de bucleback ni para otras interfaces. Para comprobar que los paquetes no aparecen en la red, siga las instrucciones de Inspección de seguimientos de red para la detección de [WS](inspecting-network-traces-for-udp-ws-discovery.md) udp y busque evidencias de mensajes de multidifusión que faltan.

## <a name="verifying-that-messages-are-being-multicast"></a>Comprobación de que los mensajes se están multidifusión

Compruebe siempre que los [mensajes de](probe-message.md) sondeo se están multidifusión. Opcionalmente, compruebe que los [mensajes Hello](hello-message.md) y [Resolve](resolve-message.md) se están multidifusión. Tenga en cuenta que no todas las aplicaciones usan Resolver mensajes. Para obtener más información sobre los patrones de mensaje usados por clientes y hosts, vea Patrones de mensajes de intercambio de [metadatos](discovery-and-metadata-exchange-message-patterns.md) y detección Tareas iniciales solución de problemas de [WSDAPI.](getting-started-with-wsdapi-troubleshooting.md)

Los mensajes se deben desencadenar para que se envíen como se describe en el paso 3 anterior. El cliente de depuración de WSD muestra el mensaje SOAP sin formato como salida. Dado que todos los mensajes impresos por el cliente de depuración de WSD en modo de multidifusión se reciben a través de un socket de multidifusión, no se muestra la dirección de destino del mensaje.

La siguiente salida del cliente de depuración WSD de ejemplo muestra un mensaje de sondeo. El \<wsa:Action> elemento identifica el mensaje como un mensaje de sondeo. Inspeccione el \<wsa:Action> campo para comprobar que el mensaje recibido era un mensaje de sondeo.

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

La siguiente salida del cliente de depuración de WSD de ejemplo muestra un mensaje Hello. El \<wsa:Action> elemento identifica el mensaje como un mensaje Hello.

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

## <a name="filtering-wsd-debug-client-results"></a>Filtrado de los resultados del cliente de depuración de WSD

Filtrar los resultados del cliente de depuración de WSD puede ayudar a identificar el tráfico de incidentes que afecta al dispositivo. El filtrado solo es necesario en redes ruidosas.

Hay dos maneras de filtrar los resultados. Las direcciones IP que se filtrarán se pueden identificar explícitamente al iniciar el cliente de depuración de WSD. Como alternativa, las direcciones IP se pueden especificar una vez iniciado el cliente. En esta sección se describen ambos métodos.

**Para especificar las direcciones IP que se filtrarán al iniciar el cliente de depuración de WSD**

1.  Configure el host y el cliente para que se ejecuten a través de la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Recopile las direcciones IP del dispositivo. Si el dispositivo tiene varias direcciones (por ejemplo, tiene direcciones IPv4 e IPv6), se deben recopilar todas las direcciones.
3.  Abra un símbolo del sistema y ejecute el siguiente comando: **WSDDebug \_client.exe /mode multicast /ip add***<device IP>*

*<device IP>* es una dirección IP. En la lista siguiente se muestran algunos formatos de ejemplo para esta dirección IP.

-   192.168.0.1
-   ::1
-   mydevice.contoso.com

El cliente de depuración de WSD resuelve automáticamente los nombres de host proporcionados en el símbolo del sistema.

**Para filtrar los resultados después de iniciar el cliente de depuración de WSD**

1.  Configure el host y el cliente para que se ejecuten a través de la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Recopile las direcciones IP del dispositivo. Si el dispositivo tiene varias direcciones (por ejemplo, tiene direcciones IPv4 e IPv6), se deben recopilar todas las direcciones.
3.  Abra un símbolo del sistema y ejecute el siguiente comando: **WSDDebug \_client.exe multidifusión /mode**
4.  En el símbolo del sistema del cliente de depuración de WSD, ejecute el siguiente comando: **ip add***<device IP>*
5.  Repita el paso 4 hasta que se hayan agregado todas las direcciones IP del dispositivo.

En el procedimiento siguiente se da por supuesto que se ha iniciado el cliente de depuración de WSD y se está filtrando por dirección IP.

**Para comprobar que se filtran las direcciones IP correctas**

-   En el símbolo del sistema del cliente de depuración de WSD, ejecute el siguiente comando: **ip print.**

    Aparece la lista de direcciones IP que se filtran.

En el procedimiento siguiente se da por supuesto que se ha iniciado el cliente de depuración de WSD y se está filtrando por dirección IP.

**Para deshabilitar el filtrado**

-   En el símbolo del sistema del cliente de depuración de WSD, ejecute el siguiente comando: **ip clear**

    Todo el tráfico de multidifusión se mostrará ahora en la salida de depuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



