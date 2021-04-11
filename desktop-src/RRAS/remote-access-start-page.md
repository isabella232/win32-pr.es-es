---
title: Acceso remoto
description: Usar el servicio de acceso remoto (RAS) para crear aplicaciones cliente.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS del servicio de acceso remoto
- RAS RAS
- RAS del servicio de acceso remoto, página de inicio
- Ras ras, consulte acceso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149102"
---
# <a name="remote-access"></a><span data-ttu-id="f019e-107">Acceso remoto</span><span class="sxs-lookup"><span data-stu-id="f019e-107">Remote Access</span></span>

## <a name="purpose"></a><span data-ttu-id="f019e-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="f019e-108">Purpose</span></span>

<span data-ttu-id="f019e-109">Usar el servicio de acceso remoto (RAS) para crear aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="f019e-109">Use Remote Access Service (RAS) to create client applications.</span></span> <span data-ttu-id="f019e-110">Estas aplicaciones muestran cuadros de diálogo comunes de RAS, administran conexiones de acceso remoto y dispositivos, y manipulan entradas de libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="f019e-110">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span> <span data-ttu-id="f019e-111">RAS también proporciona la siguiente generación de funcionalidad de servidor para el servicio de acceso remoto (RAS) para Windows.</span><span class="sxs-lookup"><span data-stu-id="f019e-111">RAS also provides the next generation of server functionality for the Remote Access Service (RAS) for Windows.</span></span> <span data-ttu-id="f019e-112">La funcionalidad del servidor RRAS sigue y se basa en el servicio de acceso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="f019e-112">The RRAS server functionality follows and builds upon the Remote Access Service (RAS).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="f019e-113">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="f019e-113">Where applicable</span></span>

<span data-ttu-id="f019e-114">El servicio de acceso remoto es aplicable en cualquier entorno informático que use un vínculo de red de área extensa (WAN) o una red privada virtual (VPN).</span><span class="sxs-lookup"><span data-stu-id="f019e-114">The Remote Access Service is applicable in any computing environment that uses a Wide Area Network (WAN) link or a Virtual Private Network (VPN).</span></span> <span data-ttu-id="f019e-115">RAS permite conectar un equipo cliente remoto a un servidor de red a través de un vínculo WAN o VPN.</span><span class="sxs-lookup"><span data-stu-id="f019e-115">RAS makes it possible to connect a remote client computer to a network server over a WAN link or a VPN.</span></span> <span data-ttu-id="f019e-116">A continuación, el equipo remoto funciona en la LAN del servidor como si el equipo remoto estuviera conectado directamente a la LAN.</span><span class="sxs-lookup"><span data-stu-id="f019e-116">The remote computer then functions on the server's LAN as though the remote computer was connected to the LAN directly.</span></span> <span data-ttu-id="f019e-117">La API de RAS permite a los programadores tener acceso a las características de RAS mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f019e-117">The RAS API enables programmers to access the features of RAS programmatically.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f019e-118">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="f019e-118">Developer audience</span></span>

<span data-ttu-id="f019e-119">La API de RAS está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="f019e-119">The RAS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="f019e-120">Los programadores de Visual Basic de Microsoft también pueden encontrar la API útil.</span><span class="sxs-lookup"><span data-stu-id="f019e-120">Microsoft Visual Basic programmers may also find the API useful.</span></span> <span data-ttu-id="f019e-121">Los programadores deben estar familiarizados con los conceptos de red.</span><span class="sxs-lookup"><span data-stu-id="f019e-121">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f019e-122">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="f019e-122">Run-time requirements</span></span>

<span data-ttu-id="f019e-123">Algunas de las funciones de la API de RAS solo se admiten en servidores de red y otras funciones solo se admiten en los clientes de red.</span><span class="sxs-lookup"><span data-stu-id="f019e-123">Some of the functions in the RAS API are supported only on network servers and other functions are supported only on network clients.</span></span> <span data-ttu-id="f019e-124">Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte las secciones de requisitos en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="f019e-124">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

<span data-ttu-id="f019e-125">La [funcionalidad de Ras mejorada](function-comparison-windows-2000-versus-rras-redistributable.md) de RRAS está disponible para Windows NT Server 4,0 mediante la instalación del [paquete redistribuible de RRAS](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span><span class="sxs-lookup"><span data-stu-id="f019e-125">The [enhanced RAS functionality](function-comparison-windows-2000-versus-rras-redistributable.md) of RRAS is available for Windows NT Server 4.0 by installing the [RRAS redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span></span> <span data-ttu-id="f019e-126">Toda la funcionalidad de RRAS se incorpora en Windows 2000 Server, Windows Server 2003 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f019e-126">All the functionality of RRAS is incorporated into Windows 2000 Server, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="f019e-127">Las aplicaciones RRAS no se pueden ejecutar en Windows NT Workstation 4,0 o en sistemas operativos cliente, como Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f019e-127">RRAS applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="f019e-128">Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte las secciones de requisitos en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="f019e-128">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f019e-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f019e-129">In this section</span></span>



| <span data-ttu-id="f019e-130">Tema</span><span class="sxs-lookup"><span data-stu-id="f019e-130">Topic</span></span>                                                                                             | <span data-ttu-id="f019e-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f019e-131">Description</span></span>                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f019e-132">Servicio de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="f019e-132">Remote Access Service</span></span>](about-remote-access-service.md)<br/>                               | <span data-ttu-id="f019e-133">El servicio de acceso remoto (RAS) proporciona funciones de acceso remoto a las aplicaciones cliente en equipos que ejecutan Windows.</span><span class="sxs-lookup"><span data-stu-id="f019e-133">Remote Access Service (RAS) provides remote access capabilities to client applications on computers running Windows.</span></span><br/>                                                                                          |
| [<span data-ttu-id="f019e-134">Administración del servicio de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="f019e-134">Remote Access Service Administration</span></span>](about-remote-access-service-administration.md)<br/> | <span data-ttu-id="f019e-135">La administración del servicio de acceso remoto proporciona un conjunto de funciones para administrar los permisos y puertos de usuario en los servidores RAS.</span><span class="sxs-lookup"><span data-stu-id="f019e-135">Remote Access Service Administration provides a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="f019e-136">Con estas funciones, puede desarrollar una aplicación de administración del servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="f019e-136">Using these functions, you can develop a RAS server administration application.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f019e-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f019e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f019e-138">Enrutamiento</span><span class="sxs-lookup"><span data-stu-id="f019e-138">Routing</span></span>](routing-start-page.md)
</dt> <dt>

[<span data-ttu-id="f019e-139">Protocolos de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="f019e-139">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

 





