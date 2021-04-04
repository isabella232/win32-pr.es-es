---
description: Los comandos Netsh para IPv6 proporcionan una herramienta de línea de comandos que puede usar para consultar y configurar interfaces, direcciones, memorias caché y rutas de IPv6. Los comandos netsh interface IPv6 se admiten en Windows XP con Service Pack 1 (SP1) y versiones posteriores.
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab092def0dc12071ee9dd62fd7554a53c9a7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154260"
---
# <a name="netshexe"></a><span data-ttu-id="30bd3-104">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="30bd3-104">Netsh.exe</span></span>

<span data-ttu-id="30bd3-105">Los comandos Netsh para IPv6 proporcionan una herramienta de línea de comandos que puede usar para consultar y configurar interfaces, direcciones, memorias caché y rutas de IPv6.</span><span class="sxs-lookup"><span data-stu-id="30bd3-105">The Netsh commands for IPv6 provide a command-line tool that you can use to query and configure IPv6 interfaces, address, caches, and routes.</span></span> <span data-ttu-id="30bd3-106">Los comandos netsh interface IPv6 se admiten en Windows XP con Service Pack 1 (SP1) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="30bd3-106">The Netsh interface IPv6 commands are supported on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="30bd3-107">Netsh.exe tiene muchos subcomandos para IPv6.</span><span class="sxs-lookup"><span data-stu-id="30bd3-107">Netsh.exe has many subcommands for IPv6.</span></span> <span data-ttu-id="30bd3-108">Puede encontrar una lista completa de las opciones de netsh interface IPv6 en el símbolo del sistema de Windows XP con SP1 y versiones posteriores; para ello, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="30bd3-108">A complete list of options for Netsh Interface IPv6 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="30bd3-109">**netsh interface IPv6/?**</span><span class="sxs-lookup"><span data-stu-id="30bd3-109">**netsh interface ipv6 /?**</span></span>

<span data-ttu-id="30bd3-110">La documentación sobre todos los comandos **netsh** para IPv6 también está disponible en línea en TechNet.</span><span class="sxs-lookup"><span data-stu-id="30bd3-110">Documentation on all of the **netsh** commands for IPv6 is also available online on Technet.</span></span> <span data-ttu-id="30bd3-111">Para obtener más información acerca de **netsh** en Windows Server 2008, vea [comandos Netsh para la interfaz (IPv4 e IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="30bd3-111">For more information on **netsh** on Windows Server 2008, please see [Netsh commands for Interface (IPv4 and IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span></span> <span data-ttu-id="30bd3-112">Para obtener más información acerca de **netsh** en Windows Server 2003, vea [comandos Netsh para la interfaz IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="30bd3-112">For more information on **netsh** on Windows Server 2003, please see [Netsh commands for Interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span></span>

<span data-ttu-id="30bd3-113">A continuación se muestran algunos comandos de uso frecuente para IPv6, aunque se admiten muchos otros comandos:</span><span class="sxs-lookup"><span data-stu-id="30bd3-113">The following are a few commonly used commands for IPv6, although many other commands are supported:</span></span>

<dl> <dt>

<span data-ttu-id="30bd3-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add Address**</span><span class="sxs-lookup"><span data-stu-id="30bd3-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-115">Agrega una dirección IPv6 a una interfaz específica en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-115">Adds an IPv6 address to a specific interface on the local computer.</span></span> <span data-ttu-id="30bd3-116">Este comando tiene parámetros de subopción que deben especificarse.</span><span class="sxs-lookup"><span data-stu-id="30bd3-116">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add DNS**</span><span class="sxs-lookup"><span data-stu-id="30bd3-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-118">Agrega una dirección IPv6 del servidor DNS a la lista de servidores DNS configurados estáticamente para la interfaz especificada en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-118">Adds a DNS server IPv6 address to the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="30bd3-119">Este comando tiene parámetros de subopción que deben especificarse.</span><span class="sxs-lookup"><span data-stu-id="30bd3-119">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add Route**</span><span class="sxs-lookup"><span data-stu-id="30bd3-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-121">Agrega una ruta para una dirección de prefijo IPv6 especificada en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-121">Adds a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="30bd3-122">Este comando tiene parámetros de subopción que deben especificarse.</span><span class="sxs-lookup"><span data-stu-id="30bd3-122">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 Delete Address**</span><span class="sxs-lookup"><span data-stu-id="30bd3-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-124">Elimina la dirección IPv6 especificada de una interfaz específica en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-124">Deletes the specified IPv6 address from a specific interface on the local computer.</span></span> <span data-ttu-id="30bd3-125">Este comando tiene parámetros de subopción que deben especificarse.</span><span class="sxs-lookup"><span data-stu-id="30bd3-125">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 Delete DNS**</span><span class="sxs-lookup"><span data-stu-id="30bd3-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-127">Elimina una dirección de servidor DNS de la lista configurada estáticamente de servidores DNS para la interfaz especificada en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-127">Deletes a DNS server address from the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="30bd3-128">Este comando tiene parámetros de subopción que deben especificarse.</span><span class="sxs-lookup"><span data-stu-id="30bd3-128">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 Delete interface**</span><span class="sxs-lookup"><span data-stu-id="30bd3-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-130">Elimina una interfaz especificada de la pila IPv6 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-130">Deletes a specified interface from the IPv6 stack on the local computer.</span></span> <span data-ttu-id="30bd3-131">Este comando tiene parámetros de subopción que deben especificarse.</span><span class="sxs-lookup"><span data-stu-id="30bd3-131">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 Delete Route**</span><span class="sxs-lookup"><span data-stu-id="30bd3-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-133">Elimina una ruta para una dirección de prefijo IPv6 especificada en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-133">Deletes a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="30bd3-134">Este comando tiene parámetros de subopción que deben especificarse.</span><span class="sxs-lookup"><span data-stu-id="30bd3-134">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**volcado de Netsh de la interfaz IPv6**</span><span class="sxs-lookup"><span data-stu-id="30bd3-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-136">Crea un script que contiene los comandos para crear la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="30bd3-136">Creates a script that contains the commands to create the current configuration.</span></span> <span data-ttu-id="30bd3-137">Si se guarda en un archivo, este script se puede usar para restaurar la configuración modificada.</span><span class="sxs-lookup"><span data-stu-id="30bd3-137">If saved to a file, this script can be used to restore altered configuration settings.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span><span class="sxs-lookup"><span data-stu-id="30bd3-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-139">Instala el protocolo IPv6 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-139">Installs the IPv6 protocol on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 Renew**</span><span class="sxs-lookup"><span data-stu-id="30bd3-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-141">Reinicia las interfaces IPv6 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-141">Restarts the IPv6 interfaces on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 RESET**</span><span class="sxs-lookup"><span data-stu-id="30bd3-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 reset**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-143">Restablece el estado de configuración de IPv6 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-143">Resets the IPv6 configuration state on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span><span class="sxs-lookup"><span data-stu-id="30bd3-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-145">Muestra los parámetros de configuración global para IPv6 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-145">Displays the global configuration parameters for IPv6 on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span><span class="sxs-lookup"><span data-stu-id="30bd3-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-147">Muestra todas las direcciones IPv6 o todas las direcciones IPv6 de una interfaz específica en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-147">Displays all IPv6 addresses or all IPv6 addresses on a specific interface on the local computer.</span></span> <span data-ttu-id="30bd3-148">Este comando tiene parámetros de subopción que pueden ser necesarios.</span><span class="sxs-lookup"><span data-stu-id="30bd3-148">This command has suboption parameters that may need to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="30bd3-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**desinstalación de netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="30bd3-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span></span>
</dt> <dd>

<span data-ttu-id="30bd3-150">Desinstala el protocolo IPv6 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="30bd3-150">Uninstalls the IPv6 protocol on the local computer.</span></span>

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a><span data-ttu-id="30bd3-151">Comandos Netsh para IPv4</span><span class="sxs-lookup"><span data-stu-id="30bd3-151">Netsh commands for IPv4</span></span>

<span data-ttu-id="30bd3-152">Los comandos Netsh similares están disponibles para IPv4.</span><span class="sxs-lookup"><span data-stu-id="30bd3-152">Similar Netsh commands are available for IPv4.</span></span> <span data-ttu-id="30bd3-153">Puede encontrar una lista completa de las opciones de los comandos Netsh para su uso con IPv4 en el símbolo del sistema de Windows XP con SP1 y versiones posteriores; para ello, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="30bd3-153">A complete list of options for Netsh commands for use with IPv4 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="30bd3-154">**netsh interface IP/?**</span><span class="sxs-lookup"><span data-stu-id="30bd3-154">**netsh interface ip /?**</span></span>

<span data-ttu-id="30bd3-155">La documentación sobre todos los comandos Netsh para IPv4 también está disponible en línea en TechNet.</span><span class="sxs-lookup"><span data-stu-id="30bd3-155">Documentation on all of the Netsh commands for IPv4 is also available online on Technet.</span></span> <span data-ttu-id="30bd3-156">Para obtener más información, consulte [comandos Netsh para la interfaz IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="30bd3-156">For more information, please see [Netsh commands for Interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span></span>

 

 
