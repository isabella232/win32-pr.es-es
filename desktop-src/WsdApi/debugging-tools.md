---
description: Un conjunto de herramientas de depuración basado en servicios web en la API de dispositivos (WSDAPI) está disponible en el Windows SDK y en el kit de controladores de Windows (WDK).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Herramientas de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156669"
---
# <a name="debugging-tools"></a>Herramientas de depuración

Un conjunto de herramientas de depuración basado en servicios web en la API de dispositivos (WSDAPI) está disponible en el Windows SDK y en el kit de controladores de Windows (WDK). Estas herramientas se pueden usar para probar la funcionalidad de las aplicaciones personalizadas escritas en WSDAPI, o los dispositivos y clientes escritos con otras pilas de perfiles de dispositivo para servicios web (DPWS).

Las herramientas host de depuración WSD (wsddebug \_host.exe) y cliente de depuración WSD (wsddebug \_client.exe) se pueden usar para inspeccionar las características de los clientes o hosts de DPWS. También se pueden usar para solucionar problemas de conectividad o configuración. Para obtener más información, consulte la [Guía de solución de problemas de WSDAPI](wsdapi-troubleshooting-guide.md). Estas herramientas solo están disponibles en el SDK de. Las herramientas del SDK se encuentran en el siguiente directorio: <Windows SDK Install Folder> \\ bin.

La [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) se puede usar para probar la interoperabilidad de nivel de SOAP o de transporte (es decir, garantizar que los mensajes tienen el formato correcto). Esta herramienta solo está disponible en el WDK.

## <a name="the-wsd-debug-client"></a>El cliente de depuración de WSD

El cliente de depuración de WSD (wsddebug \_client.exe) proporciona una consola interactiva que se puede usar para enviar y recibir mensajes WS-Discovery y para obtener metadatos. También se puede utilizar para generar y consumir mensajes de multidifusión sin procesar.

El cliente de depuración de WSD funciona en uno de estos tres modos: multidifusión, detección y metadatos.



| Mode      | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multidifusión | En el modo de multidifusión, el cliente de depuración de WSD envía y recibe mensajes de multidifusión sin formato en el puerto UDP 3702, tal y como se define en WS-Discovery. El usuario puede guardar estos mensajes SOAP en un archivo de texto y puede modificar y redifundir los mensajes con el cliente de depuración de WSD.                                                                                                                                 |
| de esquema JSON | En el modo de detección, el cliente de depuración de WSD envía y recibe mensajes de WS-Discovery con formato. Puede mostrar los mensajes [Hello](hello-message.md), [bye](bye-message.md), [ProbeMatches](probematches-message.md)y [ResolveMatches](resolvematches-message.md) recibidos. Puede enviar mensajes de [sondeo](probe-message.md) a través de UDP o http y [resolver](resolve-message.md) mensajes a través de UDP. |
| Metadatos  | Además de implementar todas las características del modo de detección, el modo de metadatos también intenta recuperar los metadatos de los dispositivos.                                                                                                                                                                                                                                                                    |



 

Para obtener más información, vea [usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md) [mediante un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md)y el [uso del cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).

## <a name="the-wsd-debug-host"></a>Host de depuración de WSD

El host de depuración de WSD (wsddebug \_host.exe) proporciona una consola interactiva que se usa para anunciar el host, responder a las solicitudes de cliente e imprimir información de diagnóstico.

El host de depuración de WSD funciona en uno de los dos modos siguientes: detección y metadatos.



| Mode      | Descripción                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| de esquema JSON | En el modo de detección, el host de depuración de WSD imprime los mensajes de WS-Discovery con formato. También envía mensajes [Hello](hello-message.md) y [bye](bye-message.md) , y responde automáticamente a los mensajes de [sondeo](probe-message.md) y [resolución](resolve-message.md) . |
| Metadatos  | Además de implementar todas las características del modo de detección, el modo de metadatos anuncia un servicio de metadatos y permite que los clientes se conecten y realicen el intercambio de metadatos.                                                                                       |



 

Para obtener más información, vea [usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md) y [usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones WSD en Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Herramientas de desarrollo de WSDAPI](wsdapi-development-tools.md)
</dt> <dt>

[Guía de solución de problemas de WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



