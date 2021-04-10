---
description: Windows Sockets 2 (Winsock) permite a los programadores crear aplicaciones avanzadas de Internet, intranet y otras aplicaciones compatibles con redes para transmitir datos de la aplicación a través de la conexión, independientemente del Protocolo de red que se use.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155256"
---
# <a name="windows-sockets-2"></a><span data-ttu-id="a2580-103">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="a2580-103">Windows Sockets 2</span></span>

## <a name="purpose"></a><span data-ttu-id="a2580-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="a2580-104">Purpose</span></span>

<span data-ttu-id="a2580-105">Windows Sockets 2 (Winsock) permite a los programadores crear aplicaciones avanzadas de Internet, intranet y otras aplicaciones compatibles con redes para transmitir datos de la aplicación a través de la conexión, independientemente del Protocolo de red que se use.</span><span class="sxs-lookup"><span data-stu-id="a2580-105">Windows Sockets 2 (Winsock) enables programmers to create advanced Internet, intranet, and other network-capable applications to transmit application data across the wire, independent of the network protocol being used.</span></span> <span data-ttu-id="a2580-106">Con Winsock, se proporciona a los programadores acceso a funciones avanzadas de redes de Microsoft® Windows®, como la multidifusión y la calidad de servicio (QoS).</span><span class="sxs-lookup"><span data-stu-id="a2580-106">With Winsock, programmers are provided access to advanced Microsoft® Windows® networking capabilities such as multicast and Quality of Service (QoS).</span></span>

<span data-ttu-id="a2580-107">Winsock sigue el modelo de Windows Open System Architecture (WOSA). define una interfaz de proveedor de servicios estándar (SPI) entre la interfaz de programación de aplicaciones (API), con sus funciones exportadas y las pilas de protocolos.</span><span class="sxs-lookup"><span data-stu-id="a2580-107">Winsock follows the Windows Open System Architecture (WOSA) model; it defines a standard service provider interface (SPI) between the application programming interface (API), with its exported functions and the protocol stacks.</span></span> <span data-ttu-id="a2580-108">Usa el paradigma de sockets que se ha usado por primera vez en Berkeley Software Distribution (BSD) UNIX.</span><span class="sxs-lookup"><span data-stu-id="a2580-108">It uses the sockets paradigm that was first popularized by Berkeley Software Distribution (BSD) UNIX.</span></span> <span data-ttu-id="a2580-109">Más adelante se adaptaba a Windows en Windows Sockets 1,1, con el que las aplicaciones de Windows Sockets 2 son compatibles con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a2580-109">It was later adapted for Windows in Windows Sockets 1.1, with which Windows Sockets 2 applications are backward compatible.</span></span> <span data-ttu-id="a2580-110">Programación de Winsock previamente centrada en torno a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a2580-110">Winsock programming previously centered around TCP/IP.</span></span> <span data-ttu-id="a2580-111">Algunas prácticas de programación que funcionan con TCP/IP no funcionan con todos los protocolos.</span><span class="sxs-lookup"><span data-stu-id="a2580-111">Some programming practices that worked with TCP/IP do not work with every protocol.</span></span> <span data-ttu-id="a2580-112">Como resultado, la API de Windows Sockets 2 agrega funciones cuando sea necesario para controlar varios protocolos.</span><span class="sxs-lookup"><span data-stu-id="a2580-112">As a result, the Windows Sockets 2 API adds functions where necessary to handle several protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a2580-113">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="a2580-113">Developer audience</span></span>

<span data-ttu-id="a2580-114">Windows Sockets 2 está diseñado para que lo usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="a2580-114">Windows Sockets 2 is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="a2580-115">Es necesario estar familiarizado con las redes de Windows.</span><span class="sxs-lookup"><span data-stu-id="a2580-115">Familiarity with Windows networking is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a2580-116">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="a2580-116">Run-time requirements</span></span>

<span data-ttu-id="a2580-117">Windows Sockets 2 se puede usar en todas las plataformas de Windows.</span><span class="sxs-lookup"><span data-stu-id="a2580-117">Windows Sockets 2 can be used on all Windows platforms.</span></span> <span data-ttu-id="a2580-118">En los casos en los que existen ciertas implementaciones o funcionalidades de las restricciones de la plataforma Windows Sockets 2, se indican claramente en la documentación.</span><span class="sxs-lookup"><span data-stu-id="a2580-118">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a2580-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a2580-119">In this section</span></span>



| <span data-ttu-id="a2580-120">Tema</span><span class="sxs-lookup"><span data-stu-id="a2580-120">Topic</span></span>                                                                                             | <span data-ttu-id="a2580-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2580-121">Description</span></span>                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2580-122">Novedades de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a2580-122">What's New for Windows Sockets</span></span>](what-s-new-for-windows-sockets-2.md)<br/>                 | <span data-ttu-id="a2580-123">Información sobre las nuevas características de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a2580-123">Information on new features for Windows Sockets.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a2580-124">Compatibilidad del Protocolo de red Winsock en Windows</span><span class="sxs-lookup"><span data-stu-id="a2580-124">Winsock Network Protocol Support in Windows</span></span>](network-protocol-support-in-windows.md)<br/> | <span data-ttu-id="a2580-125">Información sobre la compatibilidad del Protocolo de red con Windows Sockets en diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="a2580-125">Information on network protocol support for Windows Sockets on different versions of Windows.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="a2580-126">Acerca de Winsock</span><span class="sxs-lookup"><span data-stu-id="a2580-126">About Winsock</span></span>](about-winsock.md)<br/>                                                     | <span data-ttu-id="a2580-127">Información general sobre las consideraciones, la arquitectura y las capacidades de programación de Windows Sockets disponibles para los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="a2580-127">General information on Windows Sockets programming considerations, architecture, and capabilities available to developers.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="a2580-128">Usar WinSock</span><span class="sxs-lookup"><span data-stu-id="a2580-128">Using Winsock</span></span>](using-winsock.md)<br/>                                                     | <span data-ttu-id="a2580-129">Procedimientos y técnicas de programación que se usan con Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a2580-129">Procedures and programming techniques used with Windows Sockets.</span></span> <span data-ttu-id="a2580-130">Esta sección incluye técnicas básicas de programación de Winsock, como [Introducción con Winsock](getting-started-with-winsock.md), así como técnicas avanzadas útiles para los desarrolladores de Winsock con experiencia.</span><span class="sxs-lookup"><span data-stu-id="a2580-130">This section includes basic Winsock programming techniques, such as [Getting Started With Winsock](getting-started-with-winsock.md), as well as advanced techniques useful for experienced Winsock developers.</span></span><br/> |
| [<span data-ttu-id="a2580-131">Referencia de Winsock</span><span class="sxs-lookup"><span data-stu-id="a2580-131">Winsock Reference</span></span>](winsock-reference.md)<br/>                                             | <span data-ttu-id="a2580-132">Documentación de la API de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a2580-132">Documentation of the Windows Sockets API.</span></span><br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="a2580-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2580-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2580-134">Asistente IP</span><span class="sxs-lookup"><span data-stu-id="a2580-134">IP Helper</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="a2580-135">Calidad de servicio</span><span class="sxs-lookup"><span data-stu-id="a2580-135">Quality of Service</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
