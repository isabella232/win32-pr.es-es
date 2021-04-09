---
title: API HTTP Server
description: La API del servidor HTTP permite a las aplicaciones comunicarse a través de HTTP sin usar Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API HTTP Server
- API de servidor HTTP, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149265"
---
# <a name="http-server-api"></a><span data-ttu-id="8a7b0-105">API HTTP Server</span><span class="sxs-lookup"><span data-stu-id="8a7b0-105">HTTP Server API</span></span>

## <a name="purpose"></a><span data-ttu-id="8a7b0-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="8a7b0-106">Purpose</span></span>

<span data-ttu-id="8a7b0-107">La API del servidor HTTP permite a las aplicaciones comunicarse a través de HTTP sin usar Microsoft Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="8a7b0-107">The HTTP Server API enables applications to communicate over HTTP without using Microsoft Internet Information Server (IIS).</span></span> <span data-ttu-id="8a7b0-108">Las aplicaciones pueden registrarse para recibir solicitudes HTTP para direcciones URL concretas, recibir solicitudes HTTP y enviar respuestas HTTP.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-108">Applications can register to receive HTTP requests for particular URLs, receive HTTP requests, and send HTTP responses.</span></span> <span data-ttu-id="8a7b0-109">La API del servidor HTTP incluye compatibilidad con SSL para que las aplicaciones puedan intercambiar datos a través de conexiones HTTP seguras sin IIS.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-109">The HTTP Server API includes SSL support so that applications can exchange data over secure HTTP connections without IIS.</span></span> <span data-ttu-id="8a7b0-110">También está diseñado para funcionar con los puertos de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-110">It is also designed to work with I/O completion ports.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8a7b0-111">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="8a7b0-111">Developer audience</span></span>

<span data-ttu-id="8a7b0-112">Esta API está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-112">This API is designed for use by C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8a7b0-113">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="8a7b0-113">Run-time requirements</span></span>

<span data-ttu-id="8a7b0-114">La API del servidor HTTP se admite en los sistemas operativos Windows Server 2003 y en Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="8a7b0-114">The HTTP Server API is supported on Windows Server 2003 operating systems and on Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="8a7b0-115">Tenga en cuenta que Microsoft IIS 5 que se ejecuta en Windows XP con SP2 no puede compartir el puerto 80 con otras aplicaciones HTTP que se ejecutan simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-115">Be aware that Microsoft IIS 5 running on Windows XP with SP2 is not able to share port 80 with other HTTP applications running simultaneously.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a7b0-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8a7b0-116">In this section</span></span>



| <span data-ttu-id="8a7b0-117">Tema</span><span class="sxs-lookup"><span data-stu-id="8a7b0-117">Topic</span></span>                                                                           | <span data-ttu-id="8a7b0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a7b0-118">Description</span></span>                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a7b0-119">Acerca de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="8a7b0-119">About HTTP Server API</span></span>](about-http-server-api.md)<br/>                   | <span data-ttu-id="8a7b0-120">Información general sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-120">General information about HTTP.</span></span><br/>                                                              |
| [<span data-ttu-id="8a7b0-121">Uso de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="8a7b0-121">Using HTTP Server API</span></span>](using-http-server-api.md)<br/>                   | <span data-ttu-id="8a7b0-122">Guía de procedimientos para usar HTTP.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-122">Procedural guide for using HTTP.</span></span><br/>                                                             |
| [<span data-ttu-id="8a7b0-123">Referencia de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="8a7b0-123">HTTP Server API Reference</span></span>](http-server-api-reference.md)<br/>           | <span data-ttu-id="8a7b0-124">Documentación de funciones, estructuras y tipos de enumeración específicos disponibles en HTTP.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-124">Documentation of specific functions, structures, and enumeration types available in HTTP.</span></span><br/>    |
| [<span data-ttu-id="8a7b0-125">Aplicación de ejemplo de servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="8a7b0-125">HTTP Server Sample Application</span></span>](http-server-sample-application.md)<br/> | <span data-ttu-id="8a7b0-126">Una aplicación de ejemplo que muestra cómo usar la API del servidor HTTP para realizar tareas del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="8a7b0-126">A sample application that shows how to use the HTTP Server API to perform server-side tasks.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8a7b0-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a7b0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a7b0-128">Servicios HTTP de Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="8a7b0-128">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

