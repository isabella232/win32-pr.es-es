---
description: A partir de Windows Server 2008, el proveedor de características de servidor proporciona información sobre las características de servidor que están instaladas en el servidor. Esta clase permite a los administradores inventariar y administrar sus roles y características de servidor.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Proveedor de características de servidor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706458"
---
# <a name="server-feature-provider"></a><span data-ttu-id="26293-104">Proveedor de características de servidor</span><span class="sxs-lookup"><span data-stu-id="26293-104">Server Feature Provider</span></span>

<span data-ttu-id="26293-105">A partir de Windows Server 2008, el proveedor de características de servidor proporciona información sobre las características de servidor que están instaladas en el servidor.</span><span class="sxs-lookup"><span data-stu-id="26293-105">Starting with Windows Server 2008, the Server Feature Provider supplies information on what server features are installed on the server.</span></span> <span data-ttu-id="26293-106">Esta clase permite a los administradores inventariar y administrar sus roles y características de servidor.</span><span class="sxs-lookup"><span data-stu-id="26293-106">This class allows administrators to inventory and manage their server roles and features.</span></span>

<span data-ttu-id="26293-107">Un rol de servidor se define como un grupo de componentes que proporcionan funciones para un área específica de funcionalidad, como impresión, archivos, control de dominio, etc.</span><span class="sxs-lookup"><span data-stu-id="26293-107">A server role is defined as a group of components that provide functions for a specific area of functionality, such as printing, files, domain control, and so on.</span></span> <span data-ttu-id="26293-108">Los roles de servidor típicos son servidor de archivos, servidor de correo, servidor DNS, controlador de dominio, servidor de aplicaciones, etc.</span><span class="sxs-lookup"><span data-stu-id="26293-108">Typical server roles are File Server, Mail Server, DNS Server, Domain Controller, Application Server, and so on.</span></span>

<span data-ttu-id="26293-109">Si una empresa no ejecuta software de administración que informe de roles de servidor, como Microsoft Operations Manager con módulos de administración instalados, puede obtener esa información consultando la clase [**\_ ServerFeature de Win32**](win32-serverfeature.md) .</span><span class="sxs-lookup"><span data-stu-id="26293-109">If an enterprise is not running management software that reports server roles, such as Microsoft Operations Manager with management packs installed, then you can obtain that information by querying the [**Win32\_ServerFeature**](win32-serverfeature.md) class.</span></span> <span data-ttu-id="26293-110">La información de roles de servidor y características de los equipos remotos está disponible a través de las conexiones remotas WMI normales o mediante el servicio Administración remota de Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="26293-110">Server role and feature information from remote computers is available through normal WMI remote connections or by using the Windows Remote Management (WinRM) service.</span></span> <span data-ttu-id="26293-111">Para obtener más información acerca de las conexiones remotas DCOM de WMI, consulte [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="26293-111">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="26293-112">Para obtener más información sobre las conexiones que usan el protocolo [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , vea [administración remota de Windows](/windows/desktop/WinRM/portal).</span><span class="sxs-lookup"><span data-stu-id="26293-112">For more information about connections using the [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) protocol, see [Windows Remote Management](/windows/desktop/WinRM/portal).</span></span>

<span data-ttu-id="26293-113">El proveedor de características de servidor de admite las siguientes clases WMI:</span><span class="sxs-lookup"><span data-stu-id="26293-113">The Server Feature Provider supports the following WMI classes:</span></span>

-   [<span data-ttu-id="26293-114">**Win32 \_ ServerFeature**</span><span class="sxs-lookup"><span data-stu-id="26293-114">**Win32\_ServerFeature**</span></span>](win32-serverfeature.md)

## <a name="related-topics"></a><span data-ttu-id="26293-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26293-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26293-116">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="26293-116">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
