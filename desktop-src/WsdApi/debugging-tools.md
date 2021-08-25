---
description: Hay disponible un conjunto de herramientas de depuración basado en Web Services on Devices API (WSDAPI) en el SDK de Windows y el Kit de controladores de Windows (WDK).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Herramientas de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e744b37a5376d228ac9023ed7556ce63e26a7a1c20b23fb98aff090e7ae9616f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856785"
---
# <a name="debugging-tools"></a>Herramientas de depuración

Hay disponible un conjunto de herramientas de depuración basado en Web Services on Devices API (WSDAPI) en el SDK de Windows y el Kit de controladores de Windows (WDK). Estas herramientas se pueden usar para probar la funcionalidad de aplicaciones personalizadas escritas en WSDAPI, o dispositivos y clientes escritos con otras pilas de perfil de dispositivo para servicios web (DPWS).

Las herramientas WSD Debug Host (wsddebughost.exe) y \_ WSD Debug Client (wsddebugclient.exe) se pueden usar para inspeccionar las características de los clientes o hosts \_ de DPWS. También se pueden usar para solucionar problemas de conectividad o configuración. Para obtener más información, vea [WSDAPI Troubleshooting Guide](wsdapi-troubleshooting-guide.md)( Guía de solución de problemas de WSDAPI). Estas herramientas solo están disponibles en el SDK. Las herramientas del SDK se encuentran en el directorio siguiente: <Windows SDK Install Folder> \\ Bin.

La herramienta de interoperabilidad básica de [WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) se puede usar para probar la interoperabilidad de nivel de transporte o SOAP (es decir, garantizar que los mensajes están bien formados). Esta herramienta solo está disponible en wdk.

## <a name="the-wsd-debug-client"></a>El cliente de depuración de WSD

El cliente de depuración de WSD (wsddebugclient.exe) proporciona una consola interactiva que se puede usar para enviar y recibir WS-Discovery mensajes y para obtener \_ metadatos. También se puede usar para generar y consumir mensajes de multidifusión sin procesar.

El cliente de depuración de WSD funciona en uno de estos tres modos: multidifusión, detección y metadatos.



| Mode      | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multidifusión | En el modo de multidifusión, el cliente de depuración de WSD envía y recibe mensajes de multidifusión sin formato en el puerto UDP 3702, tal como se define en WS-Discovery. El usuario puede guardar estos mensajes SOAP en un archivo de texto y modificar y volver a convertir los mensajes con el cliente de depuración de WSD.                                                                                                                                 |
| Descubrimiento | En el modo de detección, el cliente de depuración de WSD envía y recibe mensajes WS-Discovery formato. Puede mostrar los mensajes [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md)y [ResolveMatches recibidos.](resolvematches-message.md) Puede enviar mensajes [de sondeo](probe-message.md) a través de UDP o HTTP, y [resolver](resolve-message.md) mensajes a través de UDP. |
| Metadatos  | Además de implementar todas las características del modo de detección, el modo metadatos también intenta recuperar metadatos de los dispositivos.                                                                                                                                                                                                                                                                    |



 

Para obtener más información, vea Using [a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), Using a Generic Host and Client for UDP [WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)y [Using WSD Debug Client](using-wsddebug-client-to-verify-multicast-traffic.md)to Verify Multicast Traffic .

## <a name="the-wsd-debug-host"></a>Host de depuración de WSD

El host de depuración de WSD (wsddebughost.exe) proporciona una consola interactiva que se usa para anunciar el host, responder a solicitudes de cliente e imprimir información \_ de diagnóstico.

El host de depuración de WSD funciona en uno de estos dos modos: detección y metadatos.



| Mode      | Descripción                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descubrimiento | En el modo de detección, el host de depuración de WSD imprime los mensajes WS-Discovery formato. También envía mensajes [hello](hello-message.md) y [bye](bye-message.md) y responde automáticamente a los mensajes [de](probe-message.md) sondeo [y resolución.](resolve-message.md) |
| Metadatos  | Además de implementar todas las características del modo de detección, el modo metadatos anuncia un servicio de metadatos y permite a los clientes conectarse y realizar el intercambio de metadatos.                                                                                       |



 

Para obtener más información, vea Using [a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and Using a Generic Host and Client for UDP [WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones WSD en Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Herramientas de desarrollo de WSDAPI](wsdapi-development-tools.md)
</dt> <dt>

[Guía de solución de problemas de WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



