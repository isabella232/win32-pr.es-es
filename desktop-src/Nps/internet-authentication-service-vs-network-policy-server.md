---
title: Servicio de autenticación de Internet & servidor de directivas de redes
description: Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104078519"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="0363f-103">Servicio de autenticación de Internet & servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="0363f-103">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="0363f-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS).</span><span class="sxs-lookup"><span data-stu-id="0363f-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="0363f-105">Servicio de autenticación Internet</span><span class="sxs-lookup"><span data-stu-id="0363f-105">Internet Authentication Service</span></span>

<span data-ttu-id="0363f-106">El servicio de autenticación de Internet es la implementación de Microsoft de un servidor RADIUS y un proxy.</span><span class="sxs-lookup"><span data-stu-id="0363f-106">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="0363f-107">El servicio de autenticación de Internet admite dos conjuntos de API: [API de extensiones de servidor de directivas de redes](ias-extensions.md) y API de objetos de datos del [servidor](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0363f-107">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="0363f-108">Consulte [technet: servicio de autenticación de Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información acerca de IAS.</span><span class="sxs-lookup"><span data-stu-id="0363f-108">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="0363f-109">Servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="0363f-109">Network Policy Server</span></span>

<span data-ttu-id="0363f-110">El servidor de directivas de redes es la implementación de Microsoft de un servidor RADIUS y un proxy, y está disponible en servidores de Windows a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0363f-110">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="0363f-111">NPS admite los mismos dos conjuntos de API que IAS: API de [extensiones de servidor de directivas de redes](ias-extensions.md) y API de objetos de datos de [servidor](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0363f-111">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="0363f-112">Además, NPS contiene un conjunto de nuevas características que amplían las capacidades de IAS.</span><span class="sxs-lookup"><span data-stu-id="0363f-112">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0363f-113">Característica</span><span class="sxs-lookup"><span data-stu-id="0363f-113">Feature</span></span></th>
<th><span data-ttu-id="0363f-114">Novedades de NPS</span><span class="sxs-lookup"><span data-stu-id="0363f-114">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0363f-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Protección de acceso a redes (NAP)</a></span><span class="sxs-lookup"><span data-stu-id="0363f-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="0363f-116">NPS es el servidor central de protección de acceso a redes.</span><span class="sxs-lookup"><span data-stu-id="0363f-116">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="0363f-117">NPS admite la creación de directivas mediante las siguientes condiciones adicionales:</span><span class="sxs-lookup"><span data-stu-id="0363f-117">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="0363f-118">Expiración de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="0363f-118">Policy expiration.</span></span></li>
<li><span data-ttu-id="0363f-119">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0363f-119">Operating system version.</span></span></li>
<li><span data-ttu-id="0363f-120">Obtener acceso a la dirección IP del cliente.</span><span class="sxs-lookup"><span data-stu-id="0363f-120">Access client IP address.</span></span></li>
<li><span data-ttu-id="0363f-121">Directivas de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0363f-121">Health policies.</span></span></li>
<li><span data-ttu-id="0363f-122">Tipos de EAP permitidos.</span><span class="sxs-lookup"><span data-stu-id="0363f-122">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="0363f-123">HCAP.</span><span class="sxs-lookup"><span data-stu-id="0363f-123">HCAP.</span></span></li>
</ul>
<span data-ttu-id="0363f-124">NPS admite la creación de directivas con la siguiente configuración adicional:</span><span class="sxs-lookup"><span data-stu-id="0363f-124">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="0363f-125">Prueba.</span><span class="sxs-lookup"><span data-stu-id="0363f-125">Probation.</span></span></li>
<li><span data-ttu-id="0363f-126">Acceso limitado.</span><span class="sxs-lookup"><span data-stu-id="0363f-126">Limited access.</span></span></li>
<li><span data-ttu-id="0363f-127">Estado extendido para el acceso limitado.</span><span class="sxs-lookup"><span data-stu-id="0363f-127">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="0363f-128">NPS, a través de NAP, interopera con CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="0363f-128">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="0363f-129">IAS no es compatible con NAP.</span><span class="sxs-lookup"><span data-stu-id="0363f-129">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0363f-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> de Compatibilidad con la Directiva y <a href="/windows/win32/eaphost/portal">EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="0363f-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="0363f-131">NPS usa EAPHost para la extensibilidad del método EAP.</span><span class="sxs-lookup"><span data-stu-id="0363f-131">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="0363f-132">Además, los administradores pueden configurar la Directiva de acceso a la red para EAP.</span><span class="sxs-lookup"><span data-stu-id="0363f-132">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="0363f-133">IAS no admite la integración de EAPHost o las condiciones de filtro de tipo de EAP para las directivas.</span><span class="sxs-lookup"><span data-stu-id="0363f-133">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0363f-134">Compatibilidad con IPv6</span><span class="sxs-lookup"><span data-stu-id="0363f-134">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="0363f-135">NPS admite la implementación en entornos IPv6.</span><span class="sxs-lookup"><span data-stu-id="0363f-135">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="0363f-136">IAS no admite direcciones de red IPv6.</span><span class="sxs-lookup"><span data-stu-id="0363f-136">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0363f-137">Configuración XML</span><span class="sxs-lookup"><span data-stu-id="0363f-137">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="0363f-138">La configuración de NPS se puede importar y exportar en formato XML.</span><span class="sxs-lookup"><span data-stu-id="0363f-138">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="0363f-139">IAS está utilizando una base de datos Jet para almacenar la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="0363f-139">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0363f-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Criterios comunes</a> Ser</span><span class="sxs-lookup"><span data-stu-id="0363f-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="0363f-141">NPS se ha actualizado para admitir su implementación en entornos que deben cumplir los estándares de seguridad de criterios comunes.</span><span class="sxs-lookup"><span data-stu-id="0363f-141">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0363f-142"><a href="ias-extensions.md">API de extensiones de NPS</a></span><span class="sxs-lookup"><span data-stu-id="0363f-142"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="0363f-143">Los archivos dll de extensión de NPS se ejecutan en un proceso independiente del servicio NPS.</span><span class="sxs-lookup"><span data-stu-id="0363f-143">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="0363f-144">Si se bloquea un archivo DLL de extensión, NPS seguirá ejecutándose y se rechazarán las solicitudes futuras.</span><span class="sxs-lookup"><span data-stu-id="0363f-144">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="0363f-145">Los archivos dll de extensión IAS se ejecutan en el mismo proceso que el servicio IAS y pueden afectar negativamente al servicio.</span><span class="sxs-lookup"><span data-stu-id="0363f-145">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0363f-146">Interfaz de usuario de administración</span><span class="sxs-lookup"><span data-stu-id="0363f-146">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="0363f-147">La consola de administración de NPS (NPS. msc) tiene un nuevo aspecto y una mejor capacidad de uso, y cubre toda la nueva funcionalidad agregada a NPS.</span><span class="sxs-lookup"><span data-stu-id="0363f-147">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="0363f-148">IAS usa la consola de administración de IAS. msc.</span><span class="sxs-lookup"><span data-stu-id="0363f-148">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0363f-149">Herramienta de administración de roles e integración de Administrador del servidor</span><span class="sxs-lookup"><span data-stu-id="0363f-149">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="0363f-150">NPS se integra con el Administrador del servidor y la herramienta de administración de roles.</span><span class="sxs-lookup"><span data-stu-id="0363f-150">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="0363f-151">Esta integración facilita la configuración y la administración de NPS y los escenarios relacionados.</span><span class="sxs-lookup"><span data-stu-id="0363f-151">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="0363f-152">Administrador del servidor no está disponible en los equipos que ejecutan IAS.</span><span class="sxs-lookup"><span data-stu-id="0363f-152">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0363f-153">Scripting de línea de comandos actualizado con <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="0363f-153">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="0363f-154">NPS es compatible con la interfaz de la &quot; línea de comandos Netsh NPS &quot; .</span><span class="sxs-lookup"><span data-stu-id="0363f-154">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="0363f-155">&quot;Netsh NPS &quot; contiene nuevos comandos que permiten configurar completamente NPS, incluidas las características de NAP.</span><span class="sxs-lookup"><span data-stu-id="0363f-155">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="0363f-156">IAS es compatible con la interfaz de la &quot; línea de comandos netsh aaaa &quot; .</span><span class="sxs-lookup"><span data-stu-id="0363f-156">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0363f-157">Aislamiento de directivas</span><span class="sxs-lookup"><span data-stu-id="0363f-157">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="0363f-158">NPS habilita la implementación del aislamiento de directivas estableciendo el origen de la Directiva de red.</span><span class="sxs-lookup"><span data-stu-id="0363f-158">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="0363f-159">Se pueden configurar directivas que solo se aplican a un tipo de NAS predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0363f-159">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="0363f-160">IAS no admite el aislamiento de directivas.</span><span class="sxs-lookup"><span data-stu-id="0363f-160">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0363f-161">Consulte [technet: servidor de directivas de redes](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información sobre NPS.</span><span class="sxs-lookup"><span data-stu-id="0363f-161">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0363f-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0363f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0363f-163">Autenticación, autorización y cuentas RADIUS</span><span class="sxs-lookup"><span data-stu-id="0363f-163">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="0363f-164">Registro con servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="0363f-164">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="0363f-165">Trabajar con un servidor de estado</span><span class="sxs-lookup"><span data-stu-id="0363f-165">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

