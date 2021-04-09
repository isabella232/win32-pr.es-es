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
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="94512-103">API del componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="94512-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="94512-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="94512-104">Purpose</span></span>

<span data-ttu-id="94512-105">La API del componente de protocolo WebSocket habilita los canales de comunicación asincrónicos y bidireccionales a través de HTTP que funcionan a través de intermediarios de red existentes.</span><span class="sxs-lookup"><span data-stu-id="94512-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="94512-106">Con la API del componente de protocolo WebSocket, un cliente usa HTTP para comunicarse con un servidor y, a continuación, ambos lados cambian a mediante el protocolo subyacente en el que se encontraba la capa HTTP (como TCP o SSL).</span><span class="sxs-lookup"><span data-stu-id="94512-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="94512-107">El objetivo es usar primero HTTP para atravesar intermediarios de red y, a continuación, usar el canal TCP/SSL subyacente de un extremo a otro para la comunicación de aplicaciones bidireccional.</span><span class="sxs-lookup"><span data-stu-id="94512-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="94512-108">El protocolo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] se define en el IETF, mientras que una API de JavaScript asociada \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] se define en el W3C.</span><span class="sxs-lookup"><span data-stu-id="94512-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="94512-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="94512-109">In this section</span></span>



| <span data-ttu-id="94512-110">Tema</span><span class="sxs-lookup"><span data-stu-id="94512-110">Topic</span></span>                                                                                                          | <span data-ttu-id="94512-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="94512-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="94512-112">**Tipos de datos de la API del componente de protocolo WebSocket**</span><span class="sxs-lookup"><span data-stu-id="94512-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="94512-113">La API del componente de protocolo WebSocket define estos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="94512-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="94512-114">Enumeraciones de API de componentes de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="94512-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="94512-115">La API del componente de protocolo WebSocket define estas enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="94512-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="94512-116">Funciones de la API del componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="94512-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="94512-117">La API del componente de protocolo WebSocket define estas funciones.</span><span class="sxs-lookup"><span data-stu-id="94512-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="94512-118">Estructuras de API de componentes de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="94512-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="94512-119">La API del componente de protocolo WebSocket define estas estructuras.</span><span class="sxs-lookup"><span data-stu-id="94512-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="94512-120">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="94512-120">Developer audience</span></span>

<span data-ttu-id="94512-121">La API del componente de protocolo WebSocket está diseñada para su uso por parte de los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="94512-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="94512-122">Es necesario estar familiarizado con las redes HTTP y Windows.</span><span class="sxs-lookup"><span data-stu-id="94512-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="94512-123">La mejor manera de usar el protocolo WebSocket en Windows es a través de la [API de servicios http de Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) o el [espacio de nombres Windows. networking. Sockets](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="94512-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="94512-124">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="94512-124">Run-time requirements</span></span>

<span data-ttu-id="94512-125">La API del componente de protocolo WebSocket requiere Windows 8 y versiones posteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="94512-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="94512-126">Las API se pueden vincular dinámicamente a través de websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="94512-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="94512-127">websocket.dll proporciona compatibilidad con los encabezados HTTP relacionados con el protocolo de enlace de cliente y servidor, comprueba los datos de protocolo de enlace recibidos y analiza el flujo de datos de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="94512-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="94512-128">No controla ninguna operación específica de HTTP (redirección, autenticación, compatibilidad con proxy) ni realizar ninguna operación de e/s (enviando o recibiendo bytes de secuencia de WebSocket).</span><span class="sxs-lookup"><span data-stu-id="94512-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="94512-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94512-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94512-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="94512-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="94512-131">Servicios HTTP de Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="94512-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

