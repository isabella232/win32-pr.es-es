---
description: La API de la aplicación auxiliar de protocolo de Internet (aplicación auxiliar de IP) permite la recuperación y modificación de la configuración de red del equipo local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Asistente de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907889"
---
# <a name="ip-helper"></a><span data-ttu-id="f18e1-103">Asistente de IP</span><span class="sxs-lookup"><span data-stu-id="f18e1-103">IP Helper</span></span>

## <a name="purpose"></a><span data-ttu-id="f18e1-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="f18e1-104">Purpose</span></span>

<span data-ttu-id="f18e1-105">La API de la aplicación auxiliar de protocolo de Internet (aplicación auxiliar de IP) permite la recuperación y modificación de la configuración de red del equipo local.</span><span class="sxs-lookup"><span data-stu-id="f18e1-105">The Internet Protocol Helper (IP Helper) API enables the retrieval and modification of network configuration settings for the local computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="f18e1-106">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="f18e1-106">Where applicable</span></span>

<span data-ttu-id="f18e1-107">La API de la aplicación auxiliar IP es aplicable en cualquier entorno informático en el que sea útil manipular mediante programación la configuración de red y TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f18e1-107">The IP Helper API is applicable in any computing environment where programmatically manipulating network and TCP/IP configuration is useful.</span></span> <span data-ttu-id="f18e1-108">Las aplicaciones típicas incluyen los protocolos de enrutamiento IP y los agentes del Protocolo simple de administración de redes (SNMP).</span><span class="sxs-lookup"><span data-stu-id="f18e1-108">Typical applications include IP routing protocols and Simple Network Management Protocol (SNMP) agents.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f18e1-109">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="f18e1-109">Developer audience</span></span>

<span data-ttu-id="f18e1-110">La API de la aplicación auxiliar de IP está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="f18e1-110">The IP Helper API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="f18e1-111">Los programadores también deben estar familiarizados con las redes de Windows y los conceptos de red TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f18e1-111">Programmers should also be familiar with Windows networking and TCP/IP networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f18e1-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="f18e1-112">Run-time requirements</span></span>

<span data-ttu-id="f18e1-113">La API auxiliar de IP se puede usar en todas las plataformas de Windows.</span><span class="sxs-lookup"><span data-stu-id="f18e1-113">The IP Helper API can be used on all Windows platforms.</span></span> <span data-ttu-id="f18e1-114">No todos los sistemas operativos admiten todas las funciones.</span><span class="sxs-lookup"><span data-stu-id="f18e1-114">Not all operating systems support all functions.</span></span> <span data-ttu-id="f18e1-115">En los casos en los que existen ciertas implementaciones o funcionalidades de las restricciones de la plataforma Windows Sockets 2, se indican claramente en la documentación.</span><span class="sxs-lookup"><span data-stu-id="f18e1-115">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span> <span data-ttu-id="f18e1-116">Si se llama a una función auxiliar de IP en una plataforma que no admite la función, \_ se devuelve el error no \_ compatible.</span><span class="sxs-lookup"><span data-stu-id="f18e1-116">If an IP Helper function is called on a platform that does not support the function, ERROR\_NOT\_SUPPORTED is returned.</span></span> <span data-ttu-id="f18e1-117">Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte las secciones de requisitos en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="f18e1-117">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f18e1-118">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f18e1-118">In this section</span></span>



| <span data-ttu-id="f18e1-119">Tema</span><span class="sxs-lookup"><span data-stu-id="f18e1-119">Topic</span></span>                                                              | <span data-ttu-id="f18e1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f18e1-120">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f18e1-121">Novedades de la aplicación auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="f18e1-121">What's New in IP Helper</span></span>](what-s-new-in-ip-helper.md)<br/>  | <span data-ttu-id="f18e1-122">Información sobre las nuevas características de la aplicación auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="f18e1-122">Information on new features for IP Helper.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="f18e1-123">Acerca de la aplicación auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="f18e1-123">About IP Helper</span></span>](about-ip-helper.md)<br/>                  | <span data-ttu-id="f18e1-124">Información general sobre las consideraciones de programación de la aplicación auxiliar IP y las capacidades disponibles para los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="f18e1-124">General information about IP Helper programming considerations and capabilities available to developers.</span></span><br/>                                                                                               |
| [<span data-ttu-id="f18e1-125">Usar la aplicación auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="f18e1-125">Using IP Helper</span></span>](using-ip-helper.md)<br/>                  | <span data-ttu-id="f18e1-126">Procedimientos y técnicas de programación que se usan con la aplicación auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="f18e1-126">Procedures and programming techniques used with IP Helper.</span></span> <span data-ttu-id="f18e1-127">Esta sección incluye técnicas básicas de programación de aplicaciones auxiliares de IP, como [Introducción con la aplicación auxiliar de IP](getting-started-with-ip-helper.md).</span><span class="sxs-lookup"><span data-stu-id="f18e1-127">This section includes basic IP Helper programming techniques, such as [Getting Started With IP Helper](getting-started-with-ip-helper.md).</span></span><br/> |
| [<span data-ttu-id="f18e1-128">Referencia de aplicación auxiliar IP</span><span class="sxs-lookup"><span data-stu-id="f18e1-128">IP Helper reference</span></span>](ip-helper-function-reference.md)<br/> | <span data-ttu-id="f18e1-129">Documentación de referencia de las funciones auxiliares de IP, estructuras y enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="f18e1-129">Reference documentation for the IP Helper functions, structures, and enumerations.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="f18e1-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f18e1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f18e1-131">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="f18e1-131">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="f18e1-132">Servicio de acceso remoto y enrutamiento</span><span class="sxs-lookup"><span data-stu-id="f18e1-132">Routing and Remote Access Service</span></span>](../rras/routing-start-page.md)
</dt> </dl>

 

