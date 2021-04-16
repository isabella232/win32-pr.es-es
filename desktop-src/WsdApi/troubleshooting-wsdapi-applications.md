---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas de las aplicaciones WSDAPI.
ms.assetid: befe4234-8d3a-4fc5-9a7d-faca94964af6
title: Solucionar problemas de otras aplicaciones de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a421f26237cc14d07a43e00faeb6d8bf49aa02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705878"
---
# <a name="troubleshooting-other-wsdapi-applications"></a>Solucionar problemas de otras aplicaciones de WSDAPI

Las aplicaciones pueden llamar directamente a las interfaces y funciones de WSDAPI para realizar la detección de dispositivos y el intercambio de metadatos. Los patrones de mensajes que utilizan estas aplicaciones varían.

El objetivo de esta guía de solución de problemas es ayudar a los desarrolladores de aplicaciones de WSDAPI a implementar correctamente un proxy de dispositivo. Esta guía no pretende ayudarle a solucionar todos los aspectos de WSDAPI. Si el proxy del dispositivo se ha creado correctamente y el cliente y el host pueden verse entre sí en la red, esta guía no puede resolver los problemas de la aplicación. Para solucionar estos problemas de aplicación, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft para obtener más ayuda.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxy"></a>Solución de problemas de clientes que llaman a WSDCreateDeviceProxy

Las aplicaciones llaman a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) para crear e inicializar una instancia de la interfaz [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . Este objeto de proxy de dispositivo se puede usar para anunciar servicios en un dispositivo y también para intercambiar metadatos.

Una aplicación que llama a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) siempre usa los siguientes mensajes.

-   [Get](get--metadata-exchange--http-request-and-message.md)
-   [GetResponse](getresponse--metadata-exchange--message.md)

A veces, una aplicación que llama a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) usa los siguientes mensajes.

-   [Resolver](resolve-message.md)
-   [ResolveMatches](resolvematches-message.md)

Los mensajes [Resolve](resolve-message.md) y [ResolveMatches](resolvematches-message.md) se generan cuando una dirección de dispositivo lógico (es decir, una dirección de dispositivo con el formato urn: UUID: {GUID}) se pasa a *pszDeviceId*. Estos mensajes no se generan cuando una dirección de dispositivo físico se pasa a *pszDeviceId*. Cuando se usan los mensajes Resolve y ResolveMatches, se envían antes que los mensajes [Get](get--metadata-exchange--http-request-and-message.md) y [GetResponse](getresponse--metadata-exchange--message.md) .

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación que llama a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) con una dirección de dispositivo física.

1.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación que llama a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) con una dirección de dispositivo lógico.

1.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).

Compruebe que los mensajes [resolver](resolve-message.md) y [ResolveMatches](resolvematches-message.md) se generan y cumplen los requisitos de tráfico. No es necesario buscar mensajes de [sondeo](probe-message.md) o [ProbeMatches](probematches-message.md) en la salida del cliente de depuración WSD o en los seguimientos de red.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxyadvanced"></a>Solución de problemas de clientes que llaman a WSDCreateDeviceProxyAdvanced

Las aplicaciones llaman a [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) para crear e inicializar una instancia de la interfaz [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . A diferencia de [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy), **WSDCreateDeviceProxyAdvanced** tiene un parámetro *pDeviceAddress* que se usa para definir la dirección de transporte del dispositivo. Si se especifica esta dirección de transporte, no se requiere la [resolución de direcciones](resolve-message.md) lógicas y no se generan los mensajes de [ResolveMatches](resolvematches-message.md) .

Si *pDeviceAddress* se establece en **null** y *pszDeviceId* es una dirección lógica, se requiere la [resolución de direcciones](resolve-message.md) y se generan los mensajes y [ResolveMatches](resolvematches-message.md) .

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación que llama a [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) con un parámetro _pDeviceAddress_ que no sea **null**. Estos procedimientos también se pueden usar cuando *pDeviceAddress* es **null** y *pszDeviceId* es una dirección física.

1.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación que llama a [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) con *PDeviceAddress* establecido en **null** y con *pszDeviceId* establecido en una dirección lógica.

1.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).

Compruebe que los mensajes [resolver](resolve-message.md) y [ResolveMatches](resolvematches-message.md) se generan y cumplen los requisitos de tráfico. No es necesario buscar mensajes de [sondeo](probe-message.md) o [ProbeMatches](probematches-message.md) en la salida del cliente de depuración WSD o en los seguimientos de red.

## <a name="troubleshooting-clients-using-the-iwsdiscoveryprovider-interface"></a>Solución de problemas de clientes mediante la interfaz IWSDiscoveryProvider

Las aplicaciones que llaman a la interfaz [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) no realizan el intercambio de metadatos. Esta interfaz solo se utiliza para la detección. Los patrones de mensajes y los procedimientos de solución de problemas son diferentes para cada método llamado en la interfaz **IWSDiscoveryProvider** .

Cuando una aplicación llama a [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype), se genera un mensaje de [sondeo](probe-message.md) . El mensaje de sondeo se envía mediante multidifusión de UDP al puerto 3702. Un mensaje [ProbeMatches](probematches-message.md) se genera como respuesta. El mensaje ProbeMatches se envía mediante unidifusión UDP y se origina en el puerto 3702.

Cuando una aplicación llama a [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid), se genera un mensaje de [resolución](resolve-message.md) . Un mensaje de resolución se envía mediante multidifusión de UDP al puerto 3702. Un mensaje [ResolveMatches](resolvematches-message.md) se genera como respuesta. La ResolveMatches se envía mediante unidifusión UDP y se origina en el puerto 3702.

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación que llama a [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) o [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid). Compruebe que los mensajes generados por la API llamada cumplen los requisitos de tráfico.

1.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).

Si una aplicación llama a [**IWSDiscoveryProvider:: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress), es una aplicación de detección dirigida. Para obtener más información sobre la solución de problemas, consulte [solución de problemas de aplicaciones con la detección dirigida](troubleshooting-applications-using-directed-discovery.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



