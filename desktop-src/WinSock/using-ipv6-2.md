---
description: En Windows XP a posterior, se proporciona una nueva herramienta de línea de comandos para configurar y administrar IPv4. Esta herramienta usa el \# comando &0034; netsh interface ip&\# 0034; para configurar y administrar IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Usar IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707116"
---
# <a name="using-ipv6"></a><span data-ttu-id="b47e3-104">Usar IPv6</span><span class="sxs-lookup"><span data-stu-id="b47e3-104">Using IPv6</span></span>

<span data-ttu-id="b47e3-105">En Windows XP a posterior, se proporciona una nueva herramienta de línea de comandos para configurar y administrar IPv4.</span><span class="sxs-lookup"><span data-stu-id="b47e3-105">On Windows XP a later, a new command-line tool is provided for configuring and managing IPv4.</span></span> <span data-ttu-id="b47e3-106">Esta herramienta usa el comando "netsh interface IP" para configurar y administrar IPv4.</span><span class="sxs-lookup"><span data-stu-id="b47e3-106">This tool uses the "netsh interface ip" command for configuring and managing IPv4.</span></span>

<span data-ttu-id="b47e3-107">En Windows XP con Service Pack 1 (SP1) y versiones posteriores, esta nueva herramienta de línea de comandos se ha mejorado para admitir la configuración y la administración de IPv6.</span><span class="sxs-lookup"><span data-stu-id="b47e3-107">On Windows XP with Service Pack 1 (SP1) and later, this new command-line tool was enhanced to support the configuration and management of IPv6.</span></span> <span data-ttu-id="b47e3-108">Esta herramienta mejorada es el comando "netsh interface IPv6".</span><span class="sxs-lookup"><span data-stu-id="b47e3-108">This enhanced tool is the "netsh interface ipv6" command.</span></span> <span data-ttu-id="b47e3-109">Los cambios de configuración realizados con los comandos Netsh.exe son permanentes y no se pierden cuando se reinicia el equipo o el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="b47e3-109">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="b47e3-110">El siguiente comando está disponible en Windows XP con SP1 y versiones posteriores para consultar y configurar IPv6 en un equipo local:</span><span class="sxs-lookup"><span data-stu-id="b47e3-110">The following command is available on Windows XP with SP1 and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="b47e3-111">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="b47e3-111">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="b47e3-112">Antes de Windows XP con Service Pack 1 (SP1), la configuración y administración de IPv6 usaba varias herramientas de línea de comandos más antiguas para configurar y administrar IPv6.</span><span class="sxs-lookup"><span data-stu-id="b47e3-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools to configure and manage IPv6.</span></span> <span data-ttu-id="b47e3-113">Con estas herramientas anteriores, los cambios de IPv6 no son permanentes y se pierden cuando se reinició el equipo o el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="b47e3-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span>

<span data-ttu-id="b47e3-114">Los siguientes comandos anteriores están disponibles en Windows XP</span><span class="sxs-lookup"><span data-stu-id="b47e3-114">The following older commands are available on Windows XP</span></span>

-   [<span data-ttu-id="b47e3-115">Net.exe</span><span class="sxs-lookup"><span data-stu-id="b47e3-115">Net.exe</span></span>](net-exe-2.md)
-   [<span data-ttu-id="b47e3-116">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="b47e3-116">Ipv6.exe</span></span>](ipv6-exe-2.md)
-   [<span data-ttu-id="b47e3-117">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="b47e3-117">Ipsec6.exe</span></span>](ipsec6-exe-2.md)

<span data-ttu-id="b47e3-118">Estas herramientas anteriores también se proporcionaron en IPv6 Technology Preview para Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b47e3-118">These older tools were also provided in the IPv6 Technology Preview for Windows 2000</span></span>

<span data-ttu-id="b47e3-119">Los cambios de configuración que usan estas herramientas anteriores se pueden mantener colocándolos como líneas de comandos en un archivo de script de comandos (. cmd) que se ejecuta después de reiniciar el equipo o el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="b47e3-119">Configuration changes using these older tools could be maintained by placing them as command lines in a command script file (.cmd) that is run after restarting the computer or the IPv6 protocol.</span></span> <span data-ttu-id="b47e3-120">Para restablecer los cambios de configuración automáticamente después del reinicio, es posible usar las tareas programadas de Windows para ejecutar el archivo. cmd cuando se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="b47e3-120">To reinstate configuration changes automatically after restarting, is was possible to use the Windows Scheduled Tasks to run the .cmd file when the computer starts.</span></span>

<span data-ttu-id="b47e3-121">Estas herramientas antiguas no se proporcionan en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b47e3-121">These older tools are not provided on Windows Server 2003 and later.</span></span> <span data-ttu-id="b47e3-122">La herramienta "netsh interface IPv6" se proporciona para configurar y administrar IPv6 desde la línea de comandos en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b47e3-122">The "netsh interface ipv6" tool is provided for configuring and managing IPv6 from the command-line on Windows Server 2003 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b47e3-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b47e3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b47e3-124">Protocolo de Internet versión 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="b47e3-124">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="b47e3-125">Guía de IPv6 para aplicaciones de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b47e3-125">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="b47e3-126">IPv6 Technology Preview para Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b47e3-126">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



