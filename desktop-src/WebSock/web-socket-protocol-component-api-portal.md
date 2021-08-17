---
title: Api de componentes del protocolo WebSocket
description: Api de componentes del protocolo WebSocket
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a712234f55b0270db9da23dc0efa1da823c85907cca92ac3428cb1225fac8a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134218"
---
# <a name="websocket-protocol-component-api"></a>Api de componentes del protocolo WebSocket

## <a name="purpose"></a>Propósito

La API de componentes del protocolo WebSocket permite canales de comunicación bidireccional asincrónicos a través de HTTP que funcionan entre los intermediarios de red existentes. Con la API de componentes del protocolo WebSocket, un cliente usa HTTP para comunicarse con un servidor y, a continuación, ambos lados cambian al uso del protocolo subyacente en el que se ha incluido HTTP en capas (como TCP o SSL). El objetivo es usar primero HTTP para atravesar los intermediarios de red y, a continuación, usar el canal TCP/SSL subyacente de un extremo a otro establecido para la comunicación bidireccional de la aplicación. El protocolo WebSocket WSPROTO se define en el IETF, mientras que una \[ [](https://tools.ietf.org/html/rfc6455) \] API de Javascript \[ [asociada W3CAPI](https://dev.w3.org/html5/websockets/) se define \] en el W3C.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                          | Descripción                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Tipos de datos de api de componentes del protocolo WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | La API del componente de protocolo WebSocket define estos tipos de datos.<br/>   |
| [Enumeraciones de api de componentes del protocolo WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | La API de componentes del protocolo WebSocket define estas enumeraciones.<br/> |
| [Funciones de api de componentes del protocolo WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | La API de componentes del protocolo WebSocket define estas funciones.<br/>    |
| [Estructuras de API de componentes del protocolo WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | La API de componentes del protocolo WebSocket define estas estructuras.<br/>   |



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de componentes del protocolo WebSocket está diseñada para su uso por parte de programadores de C/C++. Es necesario estar familiarizado con HTTP Windows redes.

> [!Note]  
> La manera preferida de usar el protocolo WebSocket en Windows es a través de Windows [HTTP Services (WinHTTP) API o](/windows/desktop/WinHttp/winhttp-start-page) [Windows. Espacio de nombres Networking.Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de componentes del protocolo WebSocket requiere Windows 8 versiones posteriores del Windows operativo. Las API se pueden vincular dinámicamente a través de websocket.dll.

> [!Note]  
> websocket.dll proporciona compatibilidad con encabezados HTTP relacionados con el protocolo de enlace de cliente y servidor, comprueba los datos de protocolo de enlace recibidos y analiza el flujo de datos de WebSocket. No controla ninguna operación específica de HTTP (redirección, autenticación, compatibilidad con proxy) ni realiza ninguna operación de E/S (enviar o recibir bytes de secuencia de WebSocket).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Windows Servicios HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

