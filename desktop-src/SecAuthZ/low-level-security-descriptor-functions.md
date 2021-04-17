---
description: Funciones para establecer y recuperar un descriptor de seguridad de objetos.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Funciones de descriptor de seguridad de bajo nivel '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669918"
---
# <a name="low-level-security-descriptor-functions"></a><span data-ttu-id="867ca-103">Funciones de descriptor de seguridad de bajo nivel </span><span class="sxs-lookup"><span data-stu-id="867ca-103">Low-level Security Descriptor Functions</span></span>

<span data-ttu-id="867ca-104">Hay varios pares de funciones de bajo nivel para establecer y recuperar el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto.</span><span class="sxs-lookup"><span data-stu-id="867ca-104">There are several pairs of low-level functions for setting and retrieving an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="867ca-105">Cada uno de estos pares solo funciona con un conjunto limitado de objetos de Windows.</span><span class="sxs-lookup"><span data-stu-id="867ca-105">Each of these pairs works only with a limited set of Windows objects.</span></span> <span data-ttu-id="867ca-106">Por ejemplo, un par funciona con objetos de archivo y otro funciona con claves del registro.</span><span class="sxs-lookup"><span data-stu-id="867ca-106">For example, one pair works with file objects and another works with registry keys.</span></span> <span data-ttu-id="867ca-107">En la tabla siguiente se muestran las funciones de bajo nivel que se usan con los distintos tipos de objetos protegibles.</span><span class="sxs-lookup"><span data-stu-id="867ca-107">The following table shows the low-level functions to use with the different types of securable objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="867ca-108">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="867ca-108">Object type</span></span></th>
<th><span data-ttu-id="867ca-109">Funciones de bajo nivel</span><span class="sxs-lookup"><span data-stu-id="867ca-109">Low-level functions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="867ca-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Archivos</a></span><span class="sxs-lookup"><span data-stu-id="867ca-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Files</a></span></span></li>
<li><span data-ttu-id="867ca-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directorios</a></span><span class="sxs-lookup"><span data-stu-id="867ca-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span></span></li>
<li><span data-ttu-id="867ca-112">Buzo</span><span class="sxs-lookup"><span data-stu-id="867ca-112">Mailslots</span></span></li>
<li><span data-ttu-id="867ca-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Canalizaciones con nombre</a></span><span class="sxs-lookup"><span data-stu-id="867ca-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipes</a></span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-114">Use las funciones <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> y <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-114">Use the <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> and <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> functions.</span></span> <span data-ttu-id="867ca-115">Estas funciones utilizan cadenas de caracteres para identificar el objeto protegible, en lugar de utilizar los identificadores.</span><span class="sxs-lookup"><span data-stu-id="867ca-115">These functions use character strings to identify the securable object, instead of using handles.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="867ca-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Procesos</a></span><span class="sxs-lookup"><span data-stu-id="867ca-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processes</a></span></span></li>
<li><span data-ttu-id="867ca-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Subprocesos</a></span><span class="sxs-lookup"><span data-stu-id="867ca-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span></span></li>
<li><span data-ttu-id="867ca-118"><a href="access-rights-for-access-token-objects.md">Tokens de acceso</a></span><span class="sxs-lookup"><span data-stu-id="867ca-118"><a href="access-rights-for-access-token-objects.md">Access tokens</a></span></span></li>
<li><span data-ttu-id="867ca-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Objetos de asignación de archivos</a></span><span class="sxs-lookup"><span data-stu-id="867ca-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-mapping objects</a></span></span></li>
<li><span data-ttu-id="867ca-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semáforos</a></span><span class="sxs-lookup"><span data-stu-id="867ca-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphores</a></span></span></li>
<li><span data-ttu-id="867ca-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Eventos</a></span><span class="sxs-lookup"><span data-stu-id="867ca-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Events</a></span></span></li>
<li><span data-ttu-id="867ca-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a> (Clases Mutex)</span><span class="sxs-lookup"><span data-stu-id="867ca-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span></span></li>
<li><span data-ttu-id="867ca-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Temporizadores que esperan</a></span><span class="sxs-lookup"><span data-stu-id="867ca-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Waitable timers</a></span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-124">Use las funciones <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> y <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-124">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="867ca-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Estaciones de ventana</a></span><span class="sxs-lookup"><span data-stu-id="867ca-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window stations</a></span></span></li>
<li><span data-ttu-id="867ca-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Escritorios</a></span><span class="sxs-lookup"><span data-stu-id="867ca-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-127">Use las funciones <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> y <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-127">Use the <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="867ca-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Claves del Registro</a></span><span class="sxs-lookup"><span data-stu-id="867ca-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry keys</a></span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-129">Use las funciones <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> y <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-129">Use the <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> and <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="867ca-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Objetos de servicio de Windows</a></span><span class="sxs-lookup"><span data-stu-id="867ca-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows service objects</a></span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-131">Use las funciones <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> y <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-131">Use the <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="867ca-132">Objetos de impresora</span><span class="sxs-lookup"><span data-stu-id="867ca-132">Printer objects</span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-133">Use la estructura <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> con las funciones <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> y <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-133">Use the <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> structure with the <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> and <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="867ca-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Recursos compartidos de red</a></span><span class="sxs-lookup"><span data-stu-id="867ca-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Network shares</a></span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-135">Use el nivel 502 con las funciones <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> y <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-135">Use level 502 with the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="867ca-136"><a href="acl-based-access-control.md">Objetos privados (objetos privados para la aplicación de creación)</a></span><span class="sxs-lookup"><span data-stu-id="867ca-136"><a href="acl-based-access-control.md">Private objects (objects private to the creating application)</a></span></span></li>
</ul></td>
<td><span data-ttu-id="867ca-137">Use las funciones <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> y <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="867ca-137">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> functions.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
