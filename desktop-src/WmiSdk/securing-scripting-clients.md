---
description: Los scripts y las aplicaciones Visual Basic deben establecer la seguridad de DCOM, especialmente para el acceso remoto, y también pueden tener que habilitar los privilegios.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Protección de los clientes de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276134"
---
# <a name="securing-scripting-clients"></a><span data-ttu-id="a5092-103">Protección de los clientes de scripting</span><span class="sxs-lookup"><span data-stu-id="a5092-103">Securing Scripting Clients</span></span>

<span data-ttu-id="a5092-104">Los scripts y las aplicaciones Visual Basic deben establecer la seguridad de DCOM, especialmente para el acceso remoto, y también pueden tener que habilitar los privilegios.</span><span class="sxs-lookup"><span data-stu-id="a5092-104">Scripts and Visual Basic applications must set DCOM security, especially for remote access, and may also need to enable privileges.</span></span>

## <a name="default-access-permissions"></a><span data-ttu-id="a5092-105">Permisos de acceso predeterminados</span><span class="sxs-lookup"><span data-stu-id="a5092-105">Default Access Permissions</span></span>

<span data-ttu-id="a5092-106">El acceso a WMI difiere entre equipos locales y remotos.</span><span class="sxs-lookup"><span data-stu-id="a5092-106">WMI access differs between local and remote computers.</span></span> <span data-ttu-id="a5092-107">Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).</span><span class="sxs-lookup"><span data-stu-id="a5092-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="a5092-108">A continuación se muestran los permisos de acceso predeterminados por cuenta:</span><span class="sxs-lookup"><span data-stu-id="a5092-108">The following are the default access permissions by account:</span></span>

-   <span data-ttu-id="a5092-109">Todos, LocalService, NetworkService</span><span class="sxs-lookup"><span data-stu-id="a5092-109">Everyone, LocalService, NetworkService</span></span>

    <span data-ttu-id="a5092-110">Permiso para leer o escribir datos y para ejecutar [*métodos de proveedor*](gloss-p.md) en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="a5092-110">Permission to read or write data and to run [*provider methods*](gloss-p.md) on the local computer.</span></span> <span data-ttu-id="a5092-111">Estas cuentas no pueden crear nuevas clases ni instalar nuevos proveedores.</span><span class="sxs-lookup"><span data-stu-id="a5092-111">These accounts cannot create new classes or install new providers.</span></span>

-   <span data-ttu-id="a5092-112">Cuentas de administrador</span><span class="sxs-lookup"><span data-stu-id="a5092-112">Administrator accounts</span></span>

    <span data-ttu-id="a5092-113">Control total en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="a5092-113">Full control on local computer.</span></span> <span data-ttu-id="a5092-114">Al conectarse a un equipo remoto, la cuenta también debe ser un administrador local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="a5092-114">When connecting to a remote computer, the account must be a local administrator on the remote computer also.</span></span>

## <a name="securing-a-scripting-client"></a><span data-ttu-id="a5092-115">Protección de un cliente de scripting</span><span class="sxs-lookup"><span data-stu-id="a5092-115">Securing a Scripting Client</span></span>

<span data-ttu-id="a5092-116">Las aplicaciones de scripting y Visual Basic de WMI deben establecer los niveles de seguridad de DCOM para los sistemas operativos que tienen como destino.</span><span class="sxs-lookup"><span data-stu-id="a5092-116">WMI scripting and Visual Basic applications must set DCOM security levels appropriately for the operating systems they are targeting.</span></span> <span data-ttu-id="a5092-117">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a5092-117">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="a5092-118">Al conectarse a un equipo remoto, es posible que tenga que cambiar el servicio (NTLM o Kerberos) que controla la autenticación.</span><span class="sxs-lookup"><span data-stu-id="a5092-118">When connecting to a remote computer, you may need to change the service (NTLM or Kerberos) that handles authentication.</span></span> <span data-ttu-id="a5092-119">Para obtener más información, vea [establecer el servicio de autenticación con VBScript](setting-the-authentication-service-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a5092-119">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md).</span></span>

<span data-ttu-id="a5092-120">El acceso a algunos datos o clases WMI puede requerir un privilegio que no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a5092-120">Access to some WMI classes or data may require a privilege that is not enabled.</span></span> <span data-ttu-id="a5092-121">Por ejemplo, debe incluir el privilegio de seguridad al conectarse a la [**clase \_ NTEventlogFile de Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a5092-121">For example, you must include the Security privilege when connecting to the [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) class.</span></span> <span data-ttu-id="a5092-122">Para obtener más información, vea [ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a5092-122">For more information, see [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="a5092-123">Si está accediendo a WMI desde una página de Active Server (ASP), se requiere cierta configuración de IIS.</span><span class="sxs-lookup"><span data-stu-id="a5092-123">If you are accessing WMI from an Active Server Page (ASP), then some IIS configuration is required.</span></span> <span data-ttu-id="a5092-124">Para obtener más información, vea [configurar IIS 5,0 y versiones posteriores para el scripting de ASP de WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="a5092-124">For more information, see [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>

<span data-ttu-id="a5092-125">Es posible que intente conectarse a un espacio de nombres que requiera una conexión cifrada, es decir, una que requiera un nivel de autenticación de pktPrivacy.</span><span class="sxs-lookup"><span data-stu-id="a5092-125">You may be trying to connect to a namespace which requires an encrypted connection, in other words, one that requires an authentication level of pktPrivacy.</span></span> <span data-ttu-id="a5092-126">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a5092-126">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
