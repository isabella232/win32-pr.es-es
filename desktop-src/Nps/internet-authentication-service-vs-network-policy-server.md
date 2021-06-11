---
title: Servicio de autenticación de Internet & servidor de directivas de red
description: Obtenga información sobre el servicio de autenticación de Internet y el servidor de directivas de red. El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd62a50021c485c7bf51cdc9caff4360e4cc863
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989430"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="5ff6d-104">Servicio de autenticación de Internet & servidor de directivas de red</span><span class="sxs-lookup"><span data-stu-id="5ff6d-104">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="5ff6d-105">El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).</span><span class="sxs-lookup"><span data-stu-id="5ff6d-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="5ff6d-106">Servicio de autenticación Internet</span><span class="sxs-lookup"><span data-stu-id="5ff6d-106">Internet Authentication Service</span></span>

<span data-ttu-id="5ff6d-107">El servicio de autenticación de Internet es la implementación de Microsoft de un servidor RADIUS y un proxy.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-107">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="5ff6d-108">El servicio de autenticación de Internet admite dos conjuntos de [API: Network Policy Server Extensions API](ias-extensions.md) y [Server Data Objects API](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5ff6d-108">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="5ff6d-109">Consulte [TechNet: Servicio de autenticación de Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información sobre IAS.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-109">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="5ff6d-110">Servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="5ff6d-110">Network Policy Server</span></span>

<span data-ttu-id="5ff6d-111">Servidor de directivas de red es la implementación de Microsoft de un servidor RADIUS y proxy y está disponible en servidores Windows a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-111">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="5ff6d-112">NPS admite los mismos dos conjuntos de API que IAS: NETWORK [Policy Server Extensions API](ias-extensions.md) y Server Data Objects [API](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5ff6d-112">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="5ff6d-113">Además, NPS contiene un conjunto de nuevas características que amplían las funcionalidades de IAS.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-113">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ff6d-114">Característica</span><span class="sxs-lookup"><span data-stu-id="5ff6d-114">Feature</span></span></th>
<th><span data-ttu-id="5ff6d-115">Novedades de NPS</span><span class="sxs-lookup"><span data-stu-id="5ff6d-115">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ff6d-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">Protección de acceso a redes (NAP)</a></span><span class="sxs-lookup"><span data-stu-id="5ff6d-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="5ff6d-117">NPS es el servidor central de Protección de acceso a redes.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-117">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="5ff6d-118">NPS admite la creación de directivas mediante las siguientes condiciones adicionales:</span><span class="sxs-lookup"><span data-stu-id="5ff6d-118">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="5ff6d-119">Expiración de la directiva.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-119">Policy expiration.</span></span></li>
<li><span data-ttu-id="5ff6d-120">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-120">Operating system version.</span></span></li>
<li><span data-ttu-id="5ff6d-121">Acceda a la dirección IP del cliente.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-121">Access client IP address.</span></span></li>
<li><span data-ttu-id="5ff6d-122">Directivas de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-122">Health policies.</span></span></li>
<li><span data-ttu-id="5ff6d-123">Tipos de EAP permitidos.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-123">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="5ff6d-124">Hcap.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-124">HCAP.</span></span></li>
</ul>
<span data-ttu-id="5ff6d-125">NPS admite la creación de directivas mediante la siguiente configuración adicional:</span><span class="sxs-lookup"><span data-stu-id="5ff6d-125">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="5ff6d-126">Libertad condicional.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-126">Probation.</span></span></li>
<li><span data-ttu-id="5ff6d-127">Acceso limitado.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-127">Limited access.</span></span></li>
<li><span data-ttu-id="5ff6d-128">Estado extendido para acceso limitado.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-128">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="5ff6d-129">NPS, a través de NAP, interopera con CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-129">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="5ff6d-130">IAS no admite NAP.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-130">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ff6d-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> Compatibilidad con <a href="/windows/win32/eaphost/portal">directivas y EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="5ff6d-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="5ff6d-132">NPS usa EAPHost para la extensibilidad del método EAP.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-132">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="5ff6d-133">Además, los administradores pueden configurar la directiva de acceso de red para EAP.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-133">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="5ff6d-134">IAS no admite la integración de EAPHost ni condiciones de filtro de tipo EAP para las directivas.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-134">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ff6d-135">Compatibilidad con IPv6</span><span class="sxs-lookup"><span data-stu-id="5ff6d-135">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="5ff6d-136">NPS admite la implementación en entornos IPv6.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-136">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="5ff6d-137">IAS no admite direcciones de red IPv6.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-137">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ff6d-138">Configuración XML</span><span class="sxs-lookup"><span data-stu-id="5ff6d-138">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="5ff6d-139">La configuración de NPS se puede importar y exportar en formato XML.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-139">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="5ff6d-140">IAS usa una base de datos Jet para almacenar la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-140">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ff6d-141"><a href="https://www.niap-ccevs.org/cc-scheme/">Criterios comunes</a> Apoyo</span><span class="sxs-lookup"><span data-stu-id="5ff6d-141"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="5ff6d-142">NPS se ha actualizado para admitir su implementación en entornos que deben cumplir los estándares de seguridad de Common Criteria.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-142">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ff6d-143"><a href="ias-extensions.md">NPS Extensions API</a></span><span class="sxs-lookup"><span data-stu-id="5ff6d-143"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="5ff6d-144">Los archivos DLL de extensión NPS se ejecutan en un proceso independiente del servicio NPS.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-144">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="5ff6d-145">Si se bloquea un archivo DLL de extensión, NPS seguirá ejecutándose y se rechazarán las solicitudes futuras.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-145">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="5ff6d-146">Los archivos DLL de extensión IAS se ejecutan en el mismo proceso que el servicio IAS y pueden afectar negativamente al servicio.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-146">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ff6d-147">Administración Interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="5ff6d-147">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="5ff6d-148">La consola de administración de NPS (nps.msc) tiene un aspecto nuevo, mejora la facilidad de uso y cubre todas las nuevas funcionalidades agregadas a NPS.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-148">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="5ff6d-149">IAS usa la consola de administración de ias.msc.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-149">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ff6d-150">Herramienta de administración de roles e Administrador del servidor integración</span><span class="sxs-lookup"><span data-stu-id="5ff6d-150">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="5ff6d-151">NPS se integra con el Administrador del servidor y la herramienta de administración de roles.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-151">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="5ff6d-152">Esta integración facilita la configuración y administración de NPS y escenarios relacionados.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-152">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="5ff6d-153">Administrador del servidor no está disponible en equipos que ejecutan IAS.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-153">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ff6d-154">Se ha actualizado el scripting de línea de comandos <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">con Netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-154">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="5ff6d-155">NPS admite la interfaz de línea de comandos &quot; nps de &quot; Netsh.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-155">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="5ff6d-156">&quot;Netsh nps &quot; contiene nuevos comandos que permiten configurar completamente NPS, incluidas las características de NAP.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-156">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="5ff6d-157">IAS admite la interfaz &quot; de la línea de comandos aaaa de &quot; Netsh.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-157">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ff6d-158">Aislamiento de directivas</span><span class="sxs-lookup"><span data-stu-id="5ff6d-158">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="5ff6d-159">NPS habilita la implementación del aislamiento de directiva estableciendo el origen de la directiva de red.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-159">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="5ff6d-160">Se pueden configurar directivas que solo son aplicables a un tipo DE NAS predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-160">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="5ff6d-161">IAS no admite el aislamiento de directivas.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-161">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5ff6d-162">Consulte [TechNet: Servidor de directivas de red](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información sobre NPS.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-162">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ff6d-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ff6d-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff6d-164">Autenticación, autorización y contabilidad RADIUS</span><span class="sxs-lookup"><span data-stu-id="5ff6d-164">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="5ff6d-165">Registro con el servidor de directivas de red</span><span class="sxs-lookup"><span data-stu-id="5ff6d-165">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="5ff6d-166">Trabajar con un servidor de estado</span><span class="sxs-lookup"><span data-stu-id="5ff6d-166">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

