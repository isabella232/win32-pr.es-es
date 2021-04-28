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
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="22df7-103">API de componentes del protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22df7-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="22df7-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="22df7-104">Purpose</span></span>

<span data-ttu-id="22df7-105">La API de componentes del protocolo WebSocket permite canales de comunicación bidireccional y asincrónicos a través de HTTP que funcionan entre los intermediarios de red existentes.</span><span class="sxs-lookup"><span data-stu-id="22df7-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="22df7-106">Con la API de componentes del protocolo WebSocket, un cliente usa HTTP para comunicarse con un servidor y, a continuación, ambos lados cambian al uso del protocolo subyacente en el que se ha distribuido HTTP por capas (por ejemplo, TCP o SSL).</span><span class="sxs-lookup"><span data-stu-id="22df7-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="22df7-107">El objetivo es usar primero HTTP para recorrer los intermediarios de red y, a continuación, usar el canal TCP/SSL subyacente de un extremo a otro establecido para la comunicación bidireccional de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="22df7-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="22df7-108">El protocolo WebSocket WSPROTO se define en el IETF, mientras que el \[ [](https://tools.ietf.org/html/rfc6455) W3CAPI de la API de Javascript asociado se define \] en el \[ [](https://dev.w3.org/html5/websockets/) \] W3C.</span><span class="sxs-lookup"><span data-stu-id="22df7-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22df7-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="22df7-109">In this section</span></span>



| <span data-ttu-id="22df7-110">Tema</span><span class="sxs-lookup"><span data-stu-id="22df7-110">Topic</span></span>                                                                                                          | <span data-ttu-id="22df7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="22df7-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="22df7-112">**Tipos de datos de api de componentes del protocolo WebSocket**</span><span class="sxs-lookup"><span data-stu-id="22df7-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="22df7-113">La API del componente de protocolo WebSocket define estos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="22df7-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="22df7-114">Enumeraciones de api de componentes del protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22df7-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="22df7-115">La API de componentes del protocolo WebSocket define estas enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="22df7-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="22df7-116">Funciones de LA API del componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22df7-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="22df7-117">La API del componente de protocolo WebSocket define estas funciones.</span><span class="sxs-lookup"><span data-stu-id="22df7-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="22df7-118">Estructuras de api de componentes del protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22df7-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="22df7-119">La API del componente de protocolo WebSocket define estas estructuras.</span><span class="sxs-lookup"><span data-stu-id="22df7-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="22df7-120">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="22df7-120">Developer audience</span></span>

<span data-ttu-id="22df7-121">La API de componentes del protocolo WebSocket está diseñada para su uso por parte de programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="22df7-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="22df7-122">Es necesario estar familiarizado con las redes HTTP y Windows.</span><span class="sxs-lookup"><span data-stu-id="22df7-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="22df7-123">La manera preferida de usar el protocolo WebSocket en Windows es a través de la API de servicios HTTP de [Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) o el espacio de nombres [Windows.Networking.Sockets](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="22df7-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="22df7-124">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="22df7-124">Run-time requirements</span></span>

<span data-ttu-id="22df7-125">La API del componente de protocolo WebSocket Windows 8 y versiones posteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="22df7-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="22df7-126">Las API se pueden vincular dinámicamente a través de websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="22df7-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="22df7-127">websocket.dll compatibilidad con encabezados HTTP relacionados con el protocolo de enlace de cliente y servidor, comprueba los datos de protocolo de enlace recibidos y analiza el flujo de datos webSocket.</span><span class="sxs-lookup"><span data-stu-id="22df7-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="22df7-128">No controla ninguna operación específica de HTTP (redirección, autenticación, compatibilidad con proxy) ni realiza ninguna operación de E/S (enviar o recibir bytes de flujo de WebSocket).</span><span class="sxs-lookup"><span data-stu-id="22df7-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="22df7-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22df7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22df7-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="22df7-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="22df7-131">Servicios HTTP de Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="22df7-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

