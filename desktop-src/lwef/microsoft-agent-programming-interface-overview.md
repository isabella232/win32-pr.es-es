---
title: Introducción a la interfaz de programación de Microsoft Agent
description: Introducción a la interfaz de programación de Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903509"
---
# <a name="microsoft-agent-programming-interface-overview"></a><span data-ttu-id="59aec-103">Introducción a la interfaz de programación de Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="59aec-103">Microsoft Agent Programming Interface Overview</span></span>

<span data-ttu-id="59aec-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="59aec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="59aec-105">La API del agente de Microsoft proporciona servicios que admiten la visualización y animación de caracteres animados.</span><span class="sxs-lookup"><span data-stu-id="59aec-105">The Microsoft Agent API provides services that support the display and animation of animated characters.</span></span> <span data-ttu-id="59aec-106">Microsoft Agent, que se implementa como un servidor de automatización OLE (modelo de objetos componentes \[ com \] ), permite que varias aplicaciones, denominadas clientes o aplicaciones cliente, hospeden y accedan a sus servicios de animación, entrada y salida al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="59aec-106">Implemented as an OLE Automation (Component Object Model \[COM\]) server, Microsoft Agent enables multiple applications, called clients or client applications, to host and access its animation, input, and output services at the same time.</span></span> <span data-ttu-id="59aec-107">Un cliente puede ser cualquier aplicación que se conecte a las interfaces COM de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="59aec-107">A client can be any application that connects to the Microsoft Agent's COM interfaces.</span></span>

<span data-ttu-id="59aec-108">Como servidor COM, el agente de Microsoft se inicia automáticamente solo cuando una aplicación cliente usa las interfaces COM y las solicitudes para conectarse a él.</span><span class="sxs-lookup"><span data-stu-id="59aec-108">As a COM server, Microsoft Agent automatically starts up only when a client application uses the COM interfaces and requests to connect to it.</span></span> <span data-ttu-id="59aec-109">Sigue ejecutándose hasta que todos los clientes cierren sus conexiones.</span><span class="sxs-lookup"><span data-stu-id="59aec-109">It remains running until all clients close their connections.</span></span> <span data-ttu-id="59aec-110">Cuando no quedan clientes conectados, el agente de Microsoft se cierra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="59aec-110">When no connected clients remain, Microsoft Agent automatically exits.</span></span>

<span data-ttu-id="59aec-111">Aunque puede llamar directamente a las interfaces COM de Microsoft Agent, el agente de Microsoft también incluye un control ActiveX de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59aec-111">Although you can call Microsoft Agent's COM interfaces directly, Microsoft Agent also includes a Microsoft ActiveX control.</span></span> <span data-ttu-id="59aec-112">Este control facilita el acceso a los servicios de Microsoft Agent desde lenguajes de programación que admiten la interfaz de control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="59aec-112">This control makes it easy to access Microsoft Agent's services from programming languages that support the ActiveX control interface.</span></span>

<span data-ttu-id="59aec-113">Además de admitir programas independientes escritos para Windows, el agente puede incluirse en scripts para admitir páginas web, siempre que el explorador admita la interfaz ActiveX.</span><span class="sxs-lookup"><span data-stu-id="59aec-113">In addition to supporting stand-alone programs written for Windows, Agent can be scripted to support webpages, provided that the browser supports the ActiveX interface.</span></span> <span data-ttu-id="59aec-114">Microsoft Internet Explorer incluye compatibilidad con ActiveX, así como con lenguajes de scripting que puede usar para programar el agente.</span><span class="sxs-lookup"><span data-stu-id="59aec-114">Microsoft Internet Explorer includes support for ActiveX as well as scripting languages that you can use to program Agent.</span></span> <span data-ttu-id="59aec-115">Si no está usando Internet Explorer, consulte con su proveedor o proveedor la compatibilidad del explorador con ActiveX.</span><span class="sxs-lookup"><span data-stu-id="59aec-115">If you are not using Internet Explorer, consult with your vendor or supplier about the browser's support for ActiveX.</span></span>

<span data-ttu-id="59aec-116">La siguiente información proporciona una breve introducción a las interfaces de programación para el software de agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59aec-116">The following information provides a brief overview of the programming interfaces for the Microsoft Agent software.</span></span>

-   [<span data-ttu-id="59aec-117">Servicios de animación</span><span class="sxs-lookup"><span data-stu-id="59aec-117">Animation Services</span></span>](animation-services.md)
-   [<span data-ttu-id="59aec-118">Servicios de entrada</span><span class="sxs-lookup"><span data-stu-id="59aec-118">Input Services</span></span>](input-services.md)
-   [<span data-ttu-id="59aec-119">Ventana comandos de voz</span><span class="sxs-lookup"><span data-stu-id="59aec-119">The Voice Commands Window</span></span>](the-voice-commands-window.md)
-   [<span data-ttu-id="59aec-120">Servicios de salida</span><span class="sxs-lookup"><span data-stu-id="59aec-120">Output Services</span></span>](output-services.md)

 

 




