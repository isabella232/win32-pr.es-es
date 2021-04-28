---
title: API de componentes del protocolo WebSocket
description: API de componentes del protocolo WebSocket
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16290a7af5b5fea406e5f47c0db718d775e4d17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088823"
---
# <a name="websocket-protocol-component-api"></a>API de componentes del protocolo WebSocket

## <a name="purpose"></a>Propósito

La API de componentes del protocolo WebSocket permite canales de comunicación bidireccional y asincrónicos a través de HTTP que funcionan entre los intermediarios de red existentes. Con la API de componentes del protocolo WebSocket, un cliente usa HTTP para comunicarse con un servidor y, a continuación, ambos lados cambian al uso del protocolo subyacente en el que se ha distribuido HTTP por capas (por ejemplo, TCP o SSL). El objetivo es usar primero HTTP para recorrer los intermediarios de red y, a continuación, usar el canal TCP/SSL subyacente de un extremo a otro establecido para la comunicación bidireccional de la aplicación. El protocolo WebSocket WSPROTO se define en el IETF, mientras que el \[ [](https://tools.ietf.org/html/rfc6455) W3CAPI de la API de Javascript asociado se define \] en el \[ [](https://dev.w3.org/html5/websockets/) \] W3C.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                          | Descripción                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Tipos de datos de api de componentes del protocolo WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | La API del componente de protocolo WebSocket define estos tipos de datos.<br/>   |
| [Enumeraciones de api de componentes del protocolo WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | La API de componentes del protocolo WebSocket define estas enumeraciones.<br/> |
| [Funciones de LA API del componente de protocolo WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | La API del componente de protocolo WebSocket define estas funciones.<br/>    |
| [Estructuras de api de componentes del protocolo WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | La API del componente de protocolo WebSocket define estas estructuras.<br/>   |



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de componentes del protocolo WebSocket está diseñada para su uso por parte de programadores de C/C++. Es necesario estar familiarizado con las redes HTTP y Windows.

> [!Note]  
> La manera preferida de usar el protocolo WebSocket en Windows es a través de la API de servicios HTTP de [Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) o el espacio de nombres [Windows.Networking.Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API del componente de protocolo WebSocket Windows 8 y versiones posteriores del sistema operativo Windows. Las API se pueden vincular dinámicamente a través de websocket.dll.

> [!Note]  
> websocket.dll compatibilidad con encabezados HTTP relacionados con el protocolo de enlace de cliente y servidor, comprueba los datos de protocolo de enlace recibidos y analiza el flujo de datos webSocket. No controla ninguna operación específica de HTTP (redirección, autenticación, compatibilidad con proxy) ni realiza ninguna operación de E/S (enviar o recibir bytes de flujo de WebSocket).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Servicios HTTP de Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

