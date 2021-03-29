---
title: Acerca de NAP
description: Acerca de NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773362"
---
# <a name="about-nap"></a><span data-ttu-id="a02fd-103">Acerca de NAP</span><span class="sxs-lookup"><span data-stu-id="a02fd-103">About NAP</span></span>

> [!Note]  
> <span data-ttu-id="a02fd-104">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a02fd-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a02fd-105">La protección de acceso a redes (NAP) está diseñada para ayudar a los administradores a mantener el estado de los equipos de la red, lo que, a su vez, ayuda a mantener la integridad general de la red.</span><span class="sxs-lookup"><span data-stu-id="a02fd-105">Network Access Protection (NAP) is designed to help administrators maintain the health of the computers on the network, which in turns helps maintain the overall integrity of the network.</span></span> <span data-ttu-id="a02fd-106">No está diseñado para proteger una red de usuarios malintencionados.</span><span class="sxs-lookup"><span data-stu-id="a02fd-106">It is not designed to secure a network from malicious users.</span></span> <span data-ttu-id="a02fd-107">Por ejemplo, si un equipo tiene todo el software y las configuraciones que requiere la Directiva de acceso a la red, el equipo se considera correcto o compatible y se le concederá el acceso adecuado a la red.</span><span class="sxs-lookup"><span data-stu-id="a02fd-107">For example, if a computer has all the software and configurations that the network access policy requires, the computer is considered healthy or compliant, and it will be granted the appropriate access to the network.</span></span> <span data-ttu-id="a02fd-108">NAP no impide que un usuario autorizado con un equipo compatible cargue un programa malintencionado a la red o que se confiere a otro comportamiento inadecuado.</span><span class="sxs-lookup"><span data-stu-id="a02fd-108">NAP does not prevent an authorized user with a compliant computer from uploading a malicious program to the network or engaging in other inappropriate behavior.</span></span>

<span data-ttu-id="a02fd-109">Para proteger el acceso a una red, una infraestructura de red debe proporcionar las siguientes áreas de funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="a02fd-109">To protect access to a network, a network infrastructure needs to provide the following areas of functionality:</span></span>

-   <span data-ttu-id="a02fd-110">Validación de estado: determina si los equipos son compatibles con los requisitos de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="a02fd-110">Health validation: Determines whether the computers are compliant with system health requirements.</span></span>
-   <span data-ttu-id="a02fd-111">Restricción de red: restringe el acceso a la red o la comunicación de los clientes que no cumplen los requisitos de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="a02fd-111">Network restriction: Restricts access to the network or communication for clients that do not comply with system health requirements.</span></span>
-   <span data-ttu-id="a02fd-112">Corrección: proporciona las actualizaciones necesarias para permitir que el equipo corrija el estado de mantenimiento no compatible.</span><span class="sxs-lookup"><span data-stu-id="a02fd-112">Remediation: Provides necessary updates to allow the computer to correct its noncompliant health state.</span></span>
-   <span data-ttu-id="a02fd-113">Cumplimiento continuo: permite el acceso a la red siempre que el equipo del usuario cumpla los requisitos de la Directiva de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="a02fd-113">Ongoing compliance: Permits access to the network as long as the user's computer meets health policy requirements.</span></span>

<span data-ttu-id="a02fd-114">Windows XP con Service Pack 3 (SP3), Windows Vista y Windows Server 2008 proporcionan métodos de cumplimiento NAP para la configuración de direcciones del Protocolo de configuración dinámica de host (DHCP), conexiones de red privada virtual (VPN) basadas en acceso remoto, conexiones cableadas e inalámbricas de IEEE 802.1 X y comunicaciones basadas en el protocolo de seguridad de Internet (IPsec).</span><span class="sxs-lookup"><span data-stu-id="a02fd-114">Windows XP with Service Pack 3 (SP3), Windows Vista, and Windows Server 2008 provide NAP enforcement methods for Dynamic Host Configuration Protocol (DHCP) address configuration, remote access-based virtual private network (VPN) connections, IEEE 802.1X-authenticated wired and wireless connections, and Internet Protocol security (IPsec)-based communications.</span></span> <span data-ttu-id="a02fd-115">Además, la plataforma NAP admite una arquitectura a través de la cual la validación de mantenimiento, la restricción de red, la corrección y el cumplimiento continuo son compatibles con componentes adicionales que pueden proporcionar otros proveedores de software o Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a02fd-115">The NAP platform additionally supports an architecture through which health validation, network restriction, remediation, and ongoing compliance are supported by additional components that can be supplied by third-party software vendors or by Microsoft.</span></span>

<span data-ttu-id="a02fd-116">La plataforma NAP incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="a02fd-116">The NAP platform includes the following components:</span></span>

-   [<span data-ttu-id="a02fd-117">Arquitectura de cliente de NAP</span><span class="sxs-lookup"><span data-stu-id="a02fd-117">NAP Client Architecture</span></span>](nap-client-architecture.md)
-   [<span data-ttu-id="a02fd-118">Arquitectura del lado servidor NAP</span><span class="sxs-lookup"><span data-stu-id="a02fd-118">NAP Server-side Architecture</span></span>](nap-server-side-architecture.md)
-   [<span data-ttu-id="a02fd-119">Comunicación de componentes del lado servidor y del cliente NAP</span><span class="sxs-lookup"><span data-stu-id="a02fd-119">NAP Client and Server-side Component Communication</span></span>](nap-client-and-server-side-component-communication.md)

<span data-ttu-id="a02fd-120">El cliente NAP requiere Windows Vista, Windows XP con SP3 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a02fd-120">The NAP client requires Windows Vista, Windows XP with SP3, or Windows Server 2008.</span></span> <span data-ttu-id="a02fd-121">El servidor de directivas de mantenimiento de NAP y los puntos de cumplimiento NAP para DHCP, VPN y cumplimiento IPsec requieren Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a02fd-121">The NAP health policy server and NAP enforcement points for DHCP, VPN, and IPsec enforcement require Windows Server 2008.</span></span>

 

 




