---
title: Servidor de directivas de redes
description: El servidor de directivas de redes (NPS) es la implementación de Microsoft de un servidor y proxy de servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359076"
---
# <a name="network-policy-server"></a><span data-ttu-id="95e22-103">Servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="95e22-103">Network Policy Server</span></span>

## <a name="purpose"></a><span data-ttu-id="95e22-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="95e22-104">Purpose</span></span>

<span data-ttu-id="95e22-105">El servidor de directivas de redes (NPS) es la implementación de Microsoft de un servidor y proxy de servicio de autenticación remota telefónica de usuario (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="95e22-105">Network Policy Server (NPS) is the Microsoft implementation of a Remote Authentication Dial-in User Service (RADIUS) server and proxy.</span></span> <span data-ttu-id="95e22-106">Es el sucesor del servicio de autenticación de Internet (IAS).</span><span class="sxs-lookup"><span data-stu-id="95e22-106">It is the successor of Internet Authentication Service (IAS).</span></span>

<span data-ttu-id="95e22-107">Como servidor RADIUS, NPS realiza la autenticación, la autorización y la administración de cuentas para conexiones de acceso remoto y de acceso telefónico y de red privada virtual (VPN).</span><span class="sxs-lookup"><span data-stu-id="95e22-107">As a RADIUS server, NPS performs authentication, authorization, and accounting for wireless, authenticating switch, and remote access dial-up and virtual private network (VPN) connections.</span></span>

<span data-ttu-id="95e22-108">NPS también es un servidor de evaluador de estado para protección de acceso a redes (NAP).</span><span class="sxs-lookup"><span data-stu-id="95e22-108">NPS is also a health evaluator server for Network Access Protection (NAP).</span></span> <span data-ttu-id="95e22-109">NPS realiza la autenticación y autorización de los intentos de conexión de red y, según las directivas de mantenimiento del sistema configuradas, evalúa el cumplimiento del estado del equipo y determina cómo limitar el acceso o la comunicación de red de un equipo no compatible.</span><span class="sxs-lookup"><span data-stu-id="95e22-109">NPS performs authentication and authorization of network connection attempts and, based on configured system health policies, evaluates computer health compliance and determines how to limit a noncompliant computer's network access or communication.</span></span> <span data-ttu-id="95e22-110">Se trata de una característica nueva específica de NPS únicamente; IAS no lo admite.</span><span class="sxs-lookup"><span data-stu-id="95e22-110">This is a new feature specific to NPS only; IAS does not support it.</span></span> <span data-ttu-id="95e22-111">Consulte [servicio de autenticación de Internet y servidor de directivas de redes](internet-authentication-service-vs-network-policy-server.md) para obtener una lista completa de las características nuevas de NPS.</span><span class="sxs-lookup"><span data-stu-id="95e22-111">See [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) for a complete list of features new to NPS.</span></span>

<span data-ttu-id="95e22-112">NPS incluye dos conjuntos de API: API de extensiones de NPS y API de objetos de datos de servidor (SDO).</span><span class="sxs-lookup"><span data-stu-id="95e22-112">NPS includes two API sets: NPS Extensions API and Server Data Objects (SDO) API.</span></span> <span data-ttu-id="95e22-113">El precursor de NPS, el servicio de autenticación de Internet, también admiten la API de extensiones de NPS y la API SDO.</span><span class="sxs-lookup"><span data-stu-id="95e22-113">Both NPS Extensions API and SDO API are also supported by the precursor of NPS, the Internet Authentication Service.</span></span>

<span data-ttu-id="95e22-114">La API de extensiones de NPS se puede usar para ampliar los métodos de autenticación, autorización y cuentas ofrecidos por NPS y antes por IAS.</span><span class="sxs-lookup"><span data-stu-id="95e22-114">NPS Extensions API can be used to extend the authentication, authorization, and accounting methods offered by NPS and previously by IAS.</span></span>

<span data-ttu-id="95e22-115">La API de objetos de datos del servidor se puede usar para manipular la configuración de la Directiva de red en un equipo que ejecuta NPS o IAS.</span><span class="sxs-lookup"><span data-stu-id="95e22-115">Server Data Objects API can be used to manipulate the network policy configuration on a computer that runs NPS or IAS.</span></span>

> [!Note]  
> <span data-ttu-id="95e22-116">Las directivas de red en NPS son equivalentes a las directivas de acceso remoto en IAS.</span><span class="sxs-lookup"><span data-stu-id="95e22-116">Network policies in NPS are equivalent to remote access policies in IAS.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="95e22-117">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="95e22-117">Developer audience</span></span>

<span data-ttu-id="95e22-118">La API de extensiones de NPS está diseñada para que la usen los programadores con el software de desarrollo de C/C++.</span><span class="sxs-lookup"><span data-stu-id="95e22-118">The NPS Extensions API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="95e22-119">Los programadores deben estar familiarizados con los conceptos de red y el protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="95e22-119">Programmers should be familiar with networking concepts and the RADIUS protocol.</span></span> <span data-ttu-id="95e22-120">RADIUS se documenta en [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) y [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="95e22-120">RADIUS is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

<span data-ttu-id="95e22-121">La API de objetos de datos del servidor está diseñada para que la usen los programadores que usan C/C++ o el software de desarrollo de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="95e22-121">The Server Data Objects API is designed for use by programmers using C/C++ or Visual Basic development software.</span></span> <span data-ttu-id="95e22-122">Los programadores deben estar familiarizados con el [servicio de acceso remoto](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) y el protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="95e22-122">Programmers should be familiar with [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) and the RADIUS protocol.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="95e22-123">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="95e22-123">Run-time requirements</span></span>

<span data-ttu-id="95e22-124">La API de extensiones de NPS se admite en Windows Server 2008 con la instalación del servicio Microsoft Commercial Internet (MCIS).</span><span class="sxs-lookup"><span data-stu-id="95e22-124">NPS Extensions API is supported on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

<span data-ttu-id="95e22-125">Server Data Objects API es compatible con Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="95e22-125">Server Data Objects API is supported on Windows Server 2008.</span></span>

<span data-ttu-id="95e22-126">NPS está disponible en Windows Server 2008 con la instalación del servicio Microsoft Commercial Internet (MCIS).</span><span class="sxs-lookup"><span data-stu-id="95e22-126">NPS is available on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="95e22-127">En esta sección</span><span class="sxs-lookup"><span data-stu-id="95e22-127">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="95e22-128">Información general</span><span class="sxs-lookup"><span data-stu-id="95e22-128">Overview</span></span>](about-network-policy-server.md)
</dt> <dd>

<span data-ttu-id="95e22-129">Información general relacionada con RADIUS, IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="95e22-129">General information regarding RADIUS, IAS, and NPS.</span></span>

</dd> <dt>

[<span data-ttu-id="95e22-130">API de extensiones de servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="95e22-130">Network Policy Server Extensions API</span></span>](ias-extensions.md)
</dt> <dd>

<span data-ttu-id="95e22-131">API para implementar archivos dll de extensión que se usan para la autenticación, autorización y cuentas.</span><span class="sxs-lookup"><span data-stu-id="95e22-131">API for implementing extension DLLs used for authentication, authorization, and accounting.</span></span>

</dd> <dt>

[<span data-ttu-id="95e22-132">Server Data Objects API</span><span class="sxs-lookup"><span data-stu-id="95e22-132">Server Data Objects API</span></span>](server-data-objects.md)
</dt> <dd>

<span data-ttu-id="95e22-133">API para administrar la configuración de la Directiva de red.</span><span class="sxs-lookup"><span data-stu-id="95e22-133">API for managing the network policy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="95e22-134">Programación de SQL</span><span class="sxs-lookup"><span data-stu-id="95e22-134">SQL Programmability</span></span>](sql-programmability.md)
</dt> <dd>

<span data-ttu-id="95e22-135">Ejemplos de procedimientos almacenados que se usan para administrar el registro de NPS (IAS).</span><span class="sxs-lookup"><span data-stu-id="95e22-135">Samples of stored procedures used for managing NPS (IAS) logging.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="95e22-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95e22-136">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="95e22-137">[TechNet: servidor de directivas de redes](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="95e22-137">[TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="95e22-138">[TechNet: servicio de autenticación de Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="95e22-138">[TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="95e22-139">Protección de acceso a redes</span><span class="sxs-lookup"><span data-stu-id="95e22-139">Network Access Protection</span></span>](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 