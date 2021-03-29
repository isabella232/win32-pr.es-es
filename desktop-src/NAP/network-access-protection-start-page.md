---
title: Protección de acceso a redes
description: 'Nota: la plataforma de protección de acceso a redes no está disponible a partir de la protección de acceso a redes (NAP) de Windows 10 es un conjunto de componentes del sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas.'
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protección de acceso a redes
- Protección de acceso a redes, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775337"
---
# <a name="network-access-protection"></a><span data-ttu-id="c2d12-105">Protección de acceso a redes</span><span class="sxs-lookup"><span data-stu-id="c2d12-105">Network Access Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="c2d12-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="c2d12-106">Purpose</span></span>

> [!Note]  
> <span data-ttu-id="c2d12-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c2d12-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c2d12-108">Protección de acceso a redes (NAP) es un conjunto de componentes del sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas.</span><span class="sxs-lookup"><span data-stu-id="c2d12-108">Network Access Protection (NAP) is a set of operating system components that provide a platform for protected access to private networks.</span></span> <span data-ttu-id="c2d12-109">La plataforma NAP proporciona una manera integrada de evaluar el estado de mantenimiento del sistema de un cliente de red que está intentando conectarse o comunicarse en una red y restringir el acceso del cliente de red hasta que se hayan cumplido los requisitos de la Directiva de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="c2d12-109">The NAP platform provides an integrated way of evaluating the system health state of a network client that is attempting to connect to or communicate on a network and restricting the access of the network client until health policy requirements have been met.</span></span>

<span data-ttu-id="c2d12-110">NAP es una plataforma extensible que proporciona una infraestructura y un conjunto de API para agregar componentes que almacenan, informan, validan y corrigen el estado de mantenimiento del sistema de un equipo.</span><span class="sxs-lookup"><span data-stu-id="c2d12-110">NAP is an extensible platform that provides an infrastructure and an API set for adding components that store, report, validate, and correct a computer's system health state.</span></span> <span data-ttu-id="c2d12-111">Por sí solo, la plataforma NAP no proporciona componentes para acumular y evaluar los atributos del estado de mantenimiento de un equipo.</span><span class="sxs-lookup"><span data-stu-id="c2d12-111">By itself, the NAP platform does not provide components to accumulate and evaluate attributes of a computer's health state.</span></span> <span data-ttu-id="c2d12-112">Otros componentes, conocidos como agentes de mantenimiento del sistema (SHA) y validadores de mantenimiento del sistema (SHV), proporcionan la validación de directivas de red y el cumplimiento de las directivas de red.</span><span class="sxs-lookup"><span data-stu-id="c2d12-112">Other components, known as system health agents (SHAs) and system health validators (SHVs), provide network policy validation and network policy compliance.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c2d12-113">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="c2d12-113">Where applicable</span></span>

<span data-ttu-id="c2d12-114">NAP está diseñado para ser extensible.</span><span class="sxs-lookup"><span data-stu-id="c2d12-114">NAP is designed to be extensible.</span></span> <span data-ttu-id="c2d12-115">Puede interoperar con cualquier software de proveedor que proporcione Sha y SHV o que reconozca su conjunto de API publicado.</span><span class="sxs-lookup"><span data-stu-id="c2d12-115">It can interoperate with any vendor software that provides SHAs and SHVs or that recognizes its published API set.</span></span> <span data-ttu-id="c2d12-116">NAP ayuda a proporcionar una solución para los siguientes escenarios comunes:</span><span class="sxs-lookup"><span data-stu-id="c2d12-116">NAP helps provide a solution for the following common scenarios:</span></span>

-   <span data-ttu-id="c2d12-117">Compruebe el estado de los equipos portátiles móviles.</span><span class="sxs-lookup"><span data-stu-id="c2d12-117">Check the health and status of roaming laptops.</span></span>
-   <span data-ttu-id="c2d12-118">Asegurarse del estado de los equipos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2d12-118">Ensure the health of desktop computers.</span></span>
-   <span data-ttu-id="c2d12-119">Compruebe el cumplimiento y el estado de los equipos de las oficinas remotas.</span><span class="sxs-lookup"><span data-stu-id="c2d12-119">Verify the compliance and health of computers in remote offices.</span></span>
-   <span data-ttu-id="c2d12-120">Determinar el estado de los equipos portátiles que se visitan.</span><span class="sxs-lookup"><span data-stu-id="c2d12-120">Determine the health of visiting laptops.</span></span>
-   <span data-ttu-id="c2d12-121">Compruebe el cumplimiento y el estado de los equipos domésticos no administrados.</span><span class="sxs-lookup"><span data-stu-id="c2d12-121">Verify the compliance and health of unmanaged home computers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c2d12-122">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="c2d12-122">Developer audience</span></span>

<span data-ttu-id="c2d12-123">La API de NAP está diseñada para desarrolladores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="c2d12-123">The NAP API is designed for C/C++ developers.</span></span> <span data-ttu-id="c2d12-124">En el caso de los métodos de cumplimiento NAP, los programadores deben estar familiarizados con los protocolos y tecnologías de red como el servicio de autenticación remota telefónica de usuario (RADIUS), el protocolo de configuración dinámica de host (DHCP), las redes privadas virtuales (VPN), el estándar IEEE 802.1 X para el acceso cableado y inalámbrico, y el protocolo de seguridad de Internet (IPsec).</span><span class="sxs-lookup"><span data-stu-id="c2d12-124">For the NAP enforcement methods, programmers should be familiar with networking protocols and technologies such as Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), virtual private networks (VPNs), the IEEE 802.1X standard for wired and wireless access, and Internet Protocol security (IPsec).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c2d12-125">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="c2d12-125">Run-time requirements</span></span>

<span data-ttu-id="c2d12-126">La plataforma NAP requiere servidores de infraestructura NAP que ejecuten Windows Server 2008 o posterior y clientes NAP que ejecuten Windows XP con Service Pack 3 (SP3), Windows Vista o sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="c2d12-126">The NAP platform requires NAP infrastructure servers running Windows Server 2008 or later and NAP clients running Windows XP with Service Pack 3 (SP3), Windows Vista, or later operating systems.</span></span> <span data-ttu-id="c2d12-127">Para obtener información específica sobre qué sistemas operativos admiten un determinado elemento de programación, consulte las secciones de requisitos de las API de NAP en la documentación de referencia de NAP.</span><span class="sxs-lookup"><span data-stu-id="c2d12-127">For specific information about which operating systems support a particular programming element, refer to the Requirements sections of the NAP APIs in the NAP Reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2d12-128">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c2d12-128">In this section</span></span>



| <span data-ttu-id="c2d12-129">Tema</span><span class="sxs-lookup"><span data-stu-id="c2d12-129">Topic</span></span>                                         | <span data-ttu-id="c2d12-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2d12-130">Description</span></span>                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c2d12-131">Acerca de NAP</span><span class="sxs-lookup"><span data-stu-id="c2d12-131">About NAP</span></span>](about-nap.md)<br/>         | <span data-ttu-id="c2d12-132">Información general sobre la API de NAP.</span><span class="sxs-lookup"><span data-stu-id="c2d12-132">General information about NAP API.</span></span><br/>                                     |
| [<span data-ttu-id="c2d12-133">Con NAP</span><span class="sxs-lookup"><span data-stu-id="c2d12-133">Using NAP</span></span>](using-nap.md)<br/>         | <span data-ttu-id="c2d12-134">Ejemplos de uso de la API de NAP.</span><span class="sxs-lookup"><span data-stu-id="c2d12-134">Usage examples for NAP API.</span></span><br/>                                            |
| [<span data-ttu-id="c2d12-135">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="c2d12-135">NAP Reference</span></span>](nap-reference.md)<br/> | <span data-ttu-id="c2d12-136">Documentación de interfaces, estructuras y otros elementos de código de NAP.</span><span class="sxs-lookup"><span data-stu-id="c2d12-136">Documentation for NAP interfaces, structures, and other code elements.</span></span><br/> |



 

 

 





