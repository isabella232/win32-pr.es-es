---
description: WMI se ejecuta como parte de un host de servicio compartido con puertos asignados a través de DCOM de forma predeterminada. Sin embargo, puede configurar el servicio WMI para que se ejecute como el único proceso en un host independiente y especifique un puerto fijo.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configuración de un puerto fijo para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717035"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a><span data-ttu-id="43008-104">Configuración de un puerto fijo para WMI</span><span class="sxs-lookup"><span data-stu-id="43008-104">Setting Up a Fixed Port for WMI</span></span>

<span data-ttu-id="43008-105">WMI se ejecuta como parte de un host de servicio compartido con puertos asignados a través de DCOM de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="43008-105">WMI runs as part of a shared service host with ports assigned through DCOM by default.</span></span> <span data-ttu-id="43008-106">Sin embargo, puede configurar el servicio WMI para que se ejecute como el único proceso en un host independiente y especifique un puerto fijo.</span><span class="sxs-lookup"><span data-stu-id="43008-106">However, you can set up the WMI service to run as the only process in a separate host and specify a fixed port.</span></span>

<span data-ttu-id="43008-107">El siguiente procedimiento es una configuración automatizada que permite a WMI tener un puerto fijo.</span><span class="sxs-lookup"><span data-stu-id="43008-107">The following procedure is an automated setup to allow WMI to have a fixed port.</span></span> <span data-ttu-id="43008-108">El procedimiento usa la herramienta de línea de comandos [**WinMgmt**](winmgmt.md) .</span><span class="sxs-lookup"><span data-stu-id="43008-108">The procedure uses the [**winmgmt**](winmgmt.md) command-line tool.</span></span>

<span data-ttu-id="43008-109">**Para configurar un puerto fijo para WMI**</span><span class="sxs-lookup"><span data-stu-id="43008-109">**To set up a fixed port for WMI**</span></span>

1.  <span data-ttu-id="43008-110">En el símbolo del sistema, escriba **WinMgmt-standalonehost**</span><span class="sxs-lookup"><span data-stu-id="43008-110">At the command prompt, type **winmgmt -standalonehost**</span></span>
2.  <span data-ttu-id="43008-111">Detenga el servicio WMI escribiendo el comando **net stop "instrumental de administración de Windows"** o use el nombre corto de **net stop WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="43008-111">Stop the WMI service by typing the command **net stop "Windows Management Instrumentation"**, or use the short name of **net stop winmgmt**</span></span>
3.  <span data-ttu-id="43008-112">Vuelva a reiniciar el servicio WMI en un nuevo host de servicio escribiendo **net start "instrumental de administración de Windows"** o **net start WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="43008-112">Restart the WMI service again in a new service host by typing **net start "Windows Management Instrumentation"** or **net start winmgmt**</span></span>
4.  <span data-ttu-id="43008-113">Establezca un nuevo número de puerto para el servicio WMI escribiendo **netsh firewall Add PORTOPENING TCP 24158 WMIFixedPort**</span><span class="sxs-lookup"><span data-stu-id="43008-113">Establish a new port number for the WMI service by typing **netsh firewall add portopening TCP 24158 WMIFixedPort**</span></span>

<span data-ttu-id="43008-114">Para deshacer los cambios que realice en WMI, escriba **WinMgmt/sharedhost** y, a continuación, detenga e inicie de nuevo el servicio WinMgmt.</span><span class="sxs-lookup"><span data-stu-id="43008-114">To undo any changes you make to WMI, type **winmgmt /sharedhost**, then stop and start the winmgmt service again.</span></span>

## <a name="examples"></a><span data-ttu-id="43008-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="43008-115">Examples</span></span>

<span data-ttu-id="43008-116">Para obtener un script que configure un puerto fijo para WMI, vea el siguiente ejemplo de [código](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )de la galería de scripting.</span><span class="sxs-lookup"><span data-stu-id="43008-116">For a script that sets up a fixed port for WMI, see the following Scripting Gallery [code sample](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span></span>

<span data-ttu-id="43008-117">o un ejemplo de código de PowerShell que habilita o deshabilita la configuración del puerto WMI, vea el ejemplo [set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) en la galería de TechNet.</span><span class="sxs-lookup"><span data-stu-id="43008-117">or a PowerShell code example that enables or disables the WMI port settings, see the [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) example on TechNet Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43008-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43008-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43008-119">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="43008-119">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="43008-120">Solución de problemas de conexiones WMI remotas</span><span class="sxs-lookup"><span data-stu-id="43008-120">Troubleshooting a Remote WMI Connections</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[<span data-ttu-id="43008-121">Hospedaje y seguridad de proveedores</span><span class="sxs-lookup"><span data-stu-id="43008-121">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



