---
title: API del componente de protocolo WebSocket
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149434"
---
# <a name="websocket-protocol-component-api"></a>API del componente de protocolo WebSocket

## <a name="purpose"></a>Propósito

La API del componente de protocolo WebSocket habilita los canales de comunicación asincrónicos y bidireccionales a través de HTTP que funcionan a través de intermediarios de red existentes. Con la API del componente de protocolo WebSocket, un cliente usa HTTP para comunicarse con un servidor y, a continuación, ambos lados cambian a mediante el protocolo subyacente en el que se encontraba la capa HTTP (como TCP o SSL). El objetivo es usar primero HTTP para atravesar intermediarios de red y, a continuación, usar el canal TCP/SSL subyacente de un extremo a otro para la comunicación de aplicaciones bidireccional. El protocolo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] se define en el IETF, mientras que una API de JavaScript asociada \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] se define en el W3C.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                          | Descripción                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Tipos de datos de la API del componente de protocolo WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | La API del componente de protocolo WebSocket define estos tipos de datos.<br/>   |
| [Enumeraciones de API de componentes de protocolo WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | La API del componente de protocolo WebSocket define estas enumeraciones.<br/> |
| [Funciones de la API del componente de protocolo WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | La API del componente de protocolo WebSocket define estas funciones.<br/>    |
| [Estructuras de API de componentes de protocolo WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | La API del componente de protocolo WebSocket define estas estructuras.<br/>   |



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API del componente de protocolo WebSocket está diseñada para su uso por parte de los programadores de C/C++. Es necesario estar familiarizado con las redes HTTP y Windows.

> [!Note]  
> La mejor manera de usar el protocolo WebSocket en Windows es a través de la [API de servicios http de Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) o el [espacio de nombres Windows. networking. Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API del componente de protocolo WebSocket requiere Windows 8 y versiones posteriores del sistema operativo Windows. Las API se pueden vincular dinámicamente a través de websocket.dll.

> [!Note]  
> websocket.dll proporciona compatibilidad con los encabezados HTTP relacionados con el protocolo de enlace de cliente y servidor, comprueba los datos de protocolo de enlace recibidos y analiza el flujo de datos de WebSocket. No controla ninguna operación específica de HTTP (redirección, autenticación, compatibilidad con proxy) ni realizar ninguna operación de e/s (enviando o recibiendo bytes de secuencia de WebSocket).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Servicios HTTP de Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

