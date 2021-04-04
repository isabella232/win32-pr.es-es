---
title: Protocolo de autenticación extensible
description: El protocolo de autenticación extensible (EAP) es un estándar que admiten varios componentes del sistema. EAP es fundamental para proteger la seguridad de la red inalámbrica (802.1 X) y las LAN cableadas, acceso telefónico y redes privadas virtuales (VPN).
ms.assetid: bdbac41e-064c-445f-8f86-a6e2eff2a683
keywords:
- Protocolo de autenticación extensible
- Protocolo de autenticación extensible, página de inicio
- EAP
- EAP, consulte protocolo de autenticación extensible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79b9585363d74eb50190d0fd6355830a7087aa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789855"
---
# <a name="extensible-authentication-protocol"></a><span data-ttu-id="1c81b-108">Protocolo de autenticación extensible</span><span class="sxs-lookup"><span data-stu-id="1c81b-108">Extensible Authentication Protocol</span></span>

## <a name="purpose"></a><span data-ttu-id="1c81b-109">Propósito</span><span class="sxs-lookup"><span data-stu-id="1c81b-109">Purpose</span></span>

<span data-ttu-id="1c81b-110">El protocolo de autenticación extensible (EAP) es un estándar que admiten varios componentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="1c81b-110">The Extensible Authentication Protocol (EAP) is a standard supported by several system components.</span></span> <span data-ttu-id="1c81b-111">EAP es fundamental para proteger la seguridad de la red inalámbrica (802.1 X) y las LAN cableadas, acceso telefónico y redes privadas virtuales (VPN).</span><span class="sxs-lookup"><span data-stu-id="1c81b-111">EAP is crucial for protecting the security of wireless (802.1X) and wired LANs, Dial-up, and Virtual Private Networks (VPNs).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1c81b-112">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="1c81b-112">Where applicable</span></span>

<span data-ttu-id="1c81b-113">EAP mejora en protocolos de autenticación anteriores como el protocolo de autenticación de contraseña (PAP) y el protocolo de autenticación por desafío mutuo (CHAP).</span><span class="sxs-lookup"><span data-stu-id="1c81b-113">EAP improves on previous authentication protocols such as Password Authentication Protocol (PAP) and Challenge Handshake Authentication Protocol (CHAP).</span></span>

<span data-ttu-id="1c81b-114">Para el nuevo desarrollo de métodos EAP, vea [host del Protocolo de autenticación extensible](../eaphost/portal.md).</span><span class="sxs-lookup"><span data-stu-id="1c81b-114">For new EAP method development, see [Extensible Authentication Protocol Host](../eaphost/portal.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1c81b-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="1c81b-115">Developer audience</span></span>

<span data-ttu-id="1c81b-116">La API EAP está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="1c81b-116">The EAP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="1c81b-117">Los programadores deben estar familiarizados con los conceptos de red.</span><span class="sxs-lookup"><span data-stu-id="1c81b-117">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1c81b-118">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="1c81b-118">Run-time requirements</span></span>

<span data-ttu-id="1c81b-119">EAP se admite en equipos cliente y servidor que se ejecutan en Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c81b-119">EAP is supported on client and server computers running on  Windows 2000 and later.</span></span> <span data-ttu-id="1c81b-120">EAP también se admite en equipos que ejecutan Windows 2000 Server y versiones posteriores si ejecutan el servicio de autenticación de Internet (IAS).</span><span class="sxs-lookup"><span data-stu-id="1c81b-120">EAP is also supported on computers running on Windows 2000 Server and later if they are running Internet Authentication Service (IAS).</span></span> <span data-ttu-id="1c81b-121">Para obtener más información acerca de los sistemas operativos compatibles, consulte la sección de requisitos en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="1c81b-121">For more information about supported operating systems, see the Requirements section in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c81b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c81b-122">Related topics</span></span>

<dl> <span data-ttu-id="1c81b-123"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1c81b-123"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1c81b-124">Servicio de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="1c81b-124">Remote Access Service</span></span>](/windows/desktop/RRAS/remote-access-start-page)
<span data-ttu-id="1c81b-125"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1c81b-125"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1c81b-126">Servicio de autenticación Internet</span><span class="sxs-lookup"><span data-stu-id="1c81b-126">Internet Authentication Service</span></span>](/windows/desktop/Nps/ias-extensions)
<span data-ttu-id="1c81b-127"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1c81b-127"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1c81b-128">Usar el protocolo de autenticación extensible</span><span class="sxs-lookup"><span data-stu-id="1c81b-128">Using Extensible Authentication Protocol</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
<span data-ttu-id="1c81b-129"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1c81b-129"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1c81b-130">Referencia del Protocolo de autenticación extensible</span><span class="sxs-lookup"><span data-stu-id="1c81b-130">Extensible Authentication Protocol Reference</span></span>](extensible-authentication-protocol-reference.md)
</dt> </dl>

 

 