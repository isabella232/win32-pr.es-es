---
title: Enrutamiento
description: Las API de enrutamiento permiten crear aplicaciones para administrar las capacidades de enrutamiento del sistema operativo.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Enrutamiento de RAS
- Enrutamiento de RAS, página de inicio
- RAS DE RRAS
- RAS de RRAS, consulte enrutamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904792"
---
# <a name="routing"></a><span data-ttu-id="1fcf2-107">Enrutamiento</span><span class="sxs-lookup"><span data-stu-id="1fcf2-107">Routing</span></span>

## <a name="purpose"></a><span data-ttu-id="1fcf2-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="1fcf2-108">Purpose</span></span>

<span data-ttu-id="1fcf2-109">Las API de enrutamiento permiten crear aplicaciones para administrar las capacidades de enrutamiento del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-109">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1fcf2-110">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="1fcf2-110">Where applicable</span></span>

<span data-ttu-id="1fcf2-111">El enrutamiento permite que un equipo funcione como un enrutador de red.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-111">Routing makes it possible for a computer to function as a network router.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1fcf2-112">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="1fcf2-112">Developer audience</span></span>

<span data-ttu-id="1fcf2-113">Las API de enrutamiento están diseñadas para que las usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-113">The Routing APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="1fcf2-114">Los programadores también deben estar familiarizados con los conceptos de red.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-114">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1fcf2-115">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="1fcf2-115">Run-time requirements</span></span>

<span data-ttu-id="1fcf2-116">El enrutamiento es una tecnología basada en servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-116">Routing is a server-based technology.</span></span> <span data-ttu-id="1fcf2-117">Toda la funcionalidad de enrutamiento se incorpora en Windows 2000 Server y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-117">All the functionality of Routing is incorporated into Windows 2000 Server and the Windows Server 2003.</span></span> <span data-ttu-id="1fcf2-118">Las aplicaciones de enrutamiento no se pueden ejecutar en Windows NT Workstation 4,0 o en sistemas operativos cliente, como Windows 95.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-118">Routing applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="1fcf2-119">Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte las secciones de requisitos en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-119">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1fcf2-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1fcf2-120">In this section</span></span>



| <span data-ttu-id="1fcf2-121">Tema</span><span class="sxs-lookup"><span data-stu-id="1fcf2-121">Topic</span></span>                                                                                               | <span data-ttu-id="1fcf2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fcf2-122">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fcf2-123">Administración de enrutadores</span><span class="sxs-lookup"><span data-stu-id="1fcf2-123">Router Management</span></span>](about-router-management.md)<br/>                                         | <span data-ttu-id="1fcf2-124">La API de administración del enrutador permite a los desarrolladores crear aplicaciones para administrar el servicio de enrutador en un equipo que ejecuta Windows 2000 Server y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-124">The router administration API allows developers to create applications to manage the router service on a computer running Windows 2000 Server and later operating systems.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="1fcf2-125">Base de información de administración y administradores de enrutadores</span><span class="sxs-lookup"><span data-stu-id="1fcf2-125">Router Managers and Management Information Base</span></span>](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | <span data-ttu-id="1fcf2-126">Las API de base de información de administración (MIB) para la administración de enrutadores permiten consultar y establecer los valores de las variables MIB exportadas por uno de los administradores de enrutadores o cualquiera de los protocolos de enrutamiento que el servicio de administradores de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="1fcf2-126">The Management Information Base (MIB) APIs for router management makes it possible to query and set the values of MIB variables exported by one of the router managers or any of the routing protocols that the router managers service.</span></span> <span data-ttu-id="1fcf2-127">Mediante esta API, el enrutador es compatible con el Protocolo simple de administración de redes (SNMP).</span><span class="sxs-lookup"><span data-stu-id="1fcf2-127">By using this API, the router supports the Simple Network Management Protocol (SNMP).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1fcf2-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fcf2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fcf2-129">Funciones de aplicación auxiliar IP</span><span class="sxs-lookup"><span data-stu-id="1fcf2-129">IP Helper Functions</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="1fcf2-130">Acceso remoto</span><span class="sxs-lookup"><span data-stu-id="1fcf2-130">Remote Access</span></span>](remote-access-start-page.md)
</dt> <dt>

[<span data-ttu-id="1fcf2-131">Protocolos de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="1fcf2-131">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

