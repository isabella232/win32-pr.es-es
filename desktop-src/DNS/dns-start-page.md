---
title: Sistema de nombres de dominio
description: Sistema de nombres de dominio (DNS), un servicio de localizador de Microsoft Windows, es un protocolo estándar del sector que busca equipos en una red basada en IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS, (véase sistema de nombres de dominio)
- Sistema de nombres de dominio
- Sistema de nombres de dominio, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104083696"
---
# <a name="domain-name-system"></a><span data-ttu-id="00f72-107">Sistema de nombres de dominio</span><span class="sxs-lookup"><span data-stu-id="00f72-107">Domain Name System</span></span>

## <a name="purpose"></a><span data-ttu-id="00f72-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="00f72-108">Purpose</span></span>

<span data-ttu-id="00f72-109">Sistema de nombres de dominio (DNS), un servicio de localizador de Microsoft Windows, es un protocolo estándar del sector que busca equipos en una red basada en IP.</span><span class="sxs-lookup"><span data-stu-id="00f72-109">Domain Name System (DNS), a locator service in Microsoft Windows, is an industry-standard protocol that locates computers on an IP-based network.</span></span> <span data-ttu-id="00f72-110">Las redes IP, como las redes de Internet y Windows, dependen de direcciones basadas en números para procesar los datos.</span><span class="sxs-lookup"><span data-stu-id="00f72-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to process data.</span></span> <span data-ttu-id="00f72-111">Sin embargo, los usuarios pueden recordar más fácilmente las direcciones de nombre, por lo que es necesario traducir nombres descriptivos (como `www.microsoft.com` ) en direcciones que la red pueda reconocer (como 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="00f72-111">Users however, can more easily remember name addresses, so it is necessary to translate user-friendly names (such as `www.microsoft.com`) into addresses that the network can recognize (such as 207.46.131.137).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="00f72-112">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="00f72-112">Where applicable</span></span>

<span data-ttu-id="00f72-113">Windows y Active Directory utilizan DNS.</span><span class="sxs-lookup"><span data-stu-id="00f72-113">Windows and Active Directory use DNS.</span></span> <span data-ttu-id="00f72-114">DNS es el servicio de localizador principal para Internet y Active Directory y, por tanto, DNS se considera un servicio base para Windows y Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00f72-114">DNS is the primary locator service for the Internet and Active Directory, and therefore, DNS is considered a base service for Windows and Active Directory.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="00f72-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="00f72-115">Developer audience</span></span>

<span data-ttu-id="00f72-116">Windows proporciona funciones que permiten a los programadores de aplicaciones usar DNS, como consultas de DNS mediante programación, comparación de registros y búsqueda de nombres.</span><span class="sxs-lookup"><span data-stu-id="00f72-116">Windows provides functions that enable application programmers to use DNS, such as programmatic DNS query, record compare, and name lookup.</span></span>

<span data-ttu-id="00f72-117">Los componentes DNS programables están diseñados para que puedan usarlos los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="00f72-117">Programmable DNS components are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="00f72-118">Para ello es necesario estar familiarizado con las redes y DNS.</span><span class="sxs-lookup"><span data-stu-id="00f72-118">Familiarity with networking and DNS is required.</span></span> <span data-ttu-id="00f72-119">Los programadores deben estar familiarizados con el conjunto de protocolos IP, así como con el protocolo DNS y las operaciones DNS.</span><span class="sxs-lookup"><span data-stu-id="00f72-119">Programmers should be familiar with the IP-protocol suite, as well as the DNS protocol and DNS operations.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="00f72-120">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="00f72-120">Run-time requirements</span></span>

<span data-ttu-id="00f72-121">DNS se usa en todas las redes IP que requieren un servicio de ubicación compatible con Internet.</span><span class="sxs-lookup"><span data-stu-id="00f72-121">DNS is used on all IP networks that require an Internet-compatible locator service.</span></span> <span data-ttu-id="00f72-122">Sin embargo, la API de DNS requiere Windows 2000 o posterior.</span><span class="sxs-lookup"><span data-stu-id="00f72-122">However, the DNS API requires Windows 2000 or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="00f72-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="00f72-123">In this section</span></span>



| <span data-ttu-id="00f72-124">Tema</span><span class="sxs-lookup"><span data-stu-id="00f72-124">Topic</span></span>                                                             | <span data-ttu-id="00f72-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="00f72-125">Description</span></span>                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="00f72-126">Documentos estándar de DNS</span><span class="sxs-lookup"><span data-stu-id="00f72-126">DNS Standards Documents</span></span>](dns-standards-documents.md)<br/> | <span data-ttu-id="00f72-127">Vínculos a documentos estándar DNS públicos.</span><span class="sxs-lookup"><span data-stu-id="00f72-127">Links to public DNS standards documents.</span></span><br/>                                  |
| [<span data-ttu-id="00f72-128">Acerca de DNS</span><span class="sxs-lookup"><span data-stu-id="00f72-128">About DNS</span></span>](about-dns.md)<br/>                             | <span data-ttu-id="00f72-129">Información general sobre DNS.</span><span class="sxs-lookup"><span data-stu-id="00f72-129">General information about DNS.</span></span><br/>                                            |
| [<span data-ttu-id="00f72-130">Referencia de DNS</span><span class="sxs-lookup"><span data-stu-id="00f72-130">DNS Reference</span></span>](dns-reference.md)<br/>                     | <span data-ttu-id="00f72-131">Documentación de referencia para DNS.</span><span class="sxs-lookup"><span data-stu-id="00f72-131">Reference documentation for DNS.</span></span><br/>                                          |
| [<span data-ttu-id="00f72-132">Proveedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="00f72-132">DNS WMI Provider</span></span>](dns-wmi-provider.md)<br/>               | <span data-ttu-id="00f72-133">Información general y documentación de referencia para el proveedor WMI de DNS.</span><span class="sxs-lookup"><span data-stu-id="00f72-133">General information and reference documentation for the DNS WMI provider.</span></span><br/> |
| [<span data-ttu-id="00f72-134">Glosario</span><span class="sxs-lookup"><span data-stu-id="00f72-134">Glossary</span></span>](glossary-gly.md)<br/>                           | <span data-ttu-id="00f72-135">Glosario de términos y definiciones de DNS.</span><span class="sxs-lookup"><span data-stu-id="00f72-135">Glossary of DNS terms and definitions.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="00f72-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00f72-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00f72-137">DHCP</span><span class="sxs-lookup"><span data-stu-id="00f72-137">DHCP</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="00f72-138">Aplicación auxiliar de protocolo de Internet</span><span class="sxs-lookup"><span data-stu-id="00f72-138">Internet Protocol Helper</span></span>](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

<span data-ttu-id="00f72-139">[Servicios de directorio](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="00f72-139">[Directory Services](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span></span>
</dt> </dl>

 

