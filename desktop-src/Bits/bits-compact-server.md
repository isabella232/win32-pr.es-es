---
title: Servidor BITS compacto
description: El servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact es un servidor de archivos HTTP/HTTPS independiente que proporciona la capacidad de transferir un número limitado de archivos grandes de forma asincrónica entre equipos.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904720"
---
# <a name="bits-compact-server"></a><span data-ttu-id="834d7-103">Servidor BITS compacto</span><span class="sxs-lookup"><span data-stu-id="834d7-103">BITS Compact Server</span></span>

<span data-ttu-id="834d7-104">El servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact es un servidor de archivos HTTP/HTTPS independiente que proporciona la capacidad de transferir un número limitado de archivos grandes de forma asincrónica entre equipos.</span><span class="sxs-lookup"><span data-stu-id="834d7-104">The Background Intelligent Transfer Service (BITS) Compact Server is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span> <span data-ttu-id="834d7-105">El servidor compacto se compila como un servicio NT y usa HTTP.SYS.</span><span class="sxs-lookup"><span data-stu-id="834d7-105">The Compact Server is built as an NT Service and uses HTTP.SYS.</span></span>

<span data-ttu-id="834d7-106">El servidor BITS compacto está diseñado para que lo usen los clientes de empresas y pequeñas empresas en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="834d7-106">The BITS Compact Server is intended for use by enterprise and small business customers under the following conditions:</span></span>

-   <span data-ttu-id="834d7-107">El uso previsto es un máximo de 25 grupos de direcciones URL, y cada grupo de direcciones URL admite 3 transferencias de archivos simultáneas.</span><span class="sxs-lookup"><span data-stu-id="834d7-107">The anticipated usage is a maximum of 25 URL groups, and each URL group supports 3 simultaneous file transfers.</span></span>
-   <span data-ttu-id="834d7-108">Las transferencias de archivos se producen entre equipos en el mismo dominio o en dominios de confianza mutua.</span><span class="sxs-lookup"><span data-stu-id="834d7-108">File transfers occur between computers in the same domain or mutually trusted domains.</span></span>
-   <span data-ttu-id="834d7-109">Las transferencias de archivos no están destinadas a clientes con conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="834d7-109">File transfers are not intended for Internet-facing clients.</span></span>

## <a name="installing-the-bits-compact-server"></a><span data-ttu-id="834d7-110">Instalación del servidor BITS compacto</span><span class="sxs-lookup"><span data-stu-id="834d7-110">Installing the BITS Compact Server</span></span>

<span data-ttu-id="834d7-111">El servidor BITS Compact es un componente de servidor opcional.</span><span class="sxs-lookup"><span data-stu-id="834d7-111">The BITS Compact Server is an optional server component.</span></span> <span data-ttu-id="834d7-112">Puede usar una de las siguientes opciones para instalar el servidor BITS compacto:</span><span class="sxs-lookup"><span data-stu-id="834d7-112">You can use one of the following options to install the BITS Compact Server:</span></span>

-   <span data-ttu-id="834d7-113">Administrador de servidores</span><span class="sxs-lookup"><span data-stu-id="834d7-113">Server Manager</span></span>

-   <span data-ttu-id="834d7-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="834d7-114">Windows PowerShell</span></span>

-   <span data-ttu-id="834d7-115">Administrador de paquetes</span><span class="sxs-lookup"><span data-stu-id="834d7-115">Package Manager</span></span>

<span data-ttu-id="834d7-116">**Para instalar el servidor BITS compacto mediante Administrador del servidor**</span><span class="sxs-lookup"><span data-stu-id="834d7-116">**To install the BITS Compact Server by using Server Manager**</span></span>

1.  <span data-ttu-id="834d7-117">En la sección **Resumen de características** del **Administrador del servidor**, haga clic en **Agregar características**.</span><span class="sxs-lookup"><span data-stu-id="834d7-117">In the **Features Summary** section of the **Server Manager**, click **Add Features**.</span></span>
2.  <span data-ttu-id="834d7-118">En el Asistente para agregar características, seleccione **servicio de transferencia inteligente en segundo plano (bits)** y **Compact Server**.</span><span class="sxs-lookup"><span data-stu-id="834d7-118">In the Add Features Wizard, select **Background Intelligent Transfer Service (BITS)** and **Compact Server**.</span></span>
3.  <span data-ttu-id="834d7-119">Siga las instrucciones del asistente, incluida la instalación del software necesario, si se indica.</span><span class="sxs-lookup"><span data-stu-id="834d7-119">Follow the wizard instructions, including installing the required software if indicated.</span></span>

<span data-ttu-id="834d7-120">Para obtener más información, consulte la ayuda en pantalla de **Administrador del servidor** .</span><span class="sxs-lookup"><span data-stu-id="834d7-120">For more information, see the **Server Manager** online help.</span></span>

<span data-ttu-id="834d7-121">**Para instalar el servidor BITS compacto mediante Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="834d7-121">**To install the BITS Compact Server by using Windows PowerShell**</span></span>

1.  <span data-ttu-id="834d7-122">En un símbolo del sistema de Windows PowerShell, escriba el siguiente comando: **Import-Module ServerManager**.</span><span class="sxs-lookup"><span data-stu-id="834d7-122">In a Windows PowerShell command prompt, type the following command: **Import-Module ServerManager**.</span></span> <span data-ttu-id="834d7-123">Luego, presione Intro.</span><span class="sxs-lookup"><span data-stu-id="834d7-123">Then press Enter.</span></span>
2.  <span data-ttu-id="834d7-124">Escriba el comando siguiente: **Add-WINDOWSFEATURE bits-Compact-Server**.</span><span class="sxs-lookup"><span data-stu-id="834d7-124">Type the following command: **Add-WindowsFeature BITS-Compact-Server**.</span></span> <span data-ttu-id="834d7-125">Luego, presione Intro.</span><span class="sxs-lookup"><span data-stu-id="834d7-125">Then press Enter.</span></span>

<span data-ttu-id="834d7-126">En el ejemplo de texto siguiente se muestra cómo instalar el servidor BITS compacto mediante cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="834d7-126">The following text-based example demonstrates installing the BITS Compact Server using Windows PowerShell cmdlets.</span></span>

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

<span data-ttu-id="834d7-127">Para obtener información sobre el uso de cmdlets, consulte la documentación de [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="834d7-127">For information about using cmdlets, see the [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentation.</span></span>

<span data-ttu-id="834d7-128">Para obtener más información sobre el cmdlet Import-Module, consulte [Import-Module](/previous-versions//dd347701(v=technet.10)) en la biblioteca de Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="834d7-128">For more information about the Import-Module cmdlet, see [Import-Module](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="834d7-129">Para obtener ayuda en la línea de comandos, escriba **Get-Help Import-Module**.</span><span class="sxs-lookup"><span data-stu-id="834d7-129">For help at the command line, type **get-help import-module**.</span></span>

<span data-ttu-id="834d7-130">Para obtener más información sobre el cmdlet Add-WindowsFeature, consulte [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) en la biblioteca de Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="834d7-130">For more information about the Add-WindowsFeature cmdlet, see [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="834d7-131">Para obtener ayuda en la línea de comandos, escriba **Get-Help Add-WindowsFeature**.</span><span class="sxs-lookup"><span data-stu-id="834d7-131">For help at the command line, type **get-help Add-WindowsFeature**.</span></span>

<span data-ttu-id="834d7-132">**Para instalar el servidor BITS compacto mediante el administrador de paquetes**</span><span class="sxs-lookup"><span data-stu-id="834d7-132">**To install the BITS Compact Server by using Package Manager**</span></span>

-   <span data-ttu-id="834d7-133">Escriba el siguiente comando: **PkgMgr.exe/IU: LightweightServer**.</span><span class="sxs-lookup"><span data-stu-id="834d7-133">Enter the following command: **PkgMgr.exe /iu:LightweightServer**.</span></span>

> [!Note]  
> <span data-ttu-id="834d7-134">La configuración se pierde si se reinicia el servicio del servidor compacto o si se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="834d7-134">The settings are lost if the Compact Server service is restarted or if the computer is rebooted.</span></span>

 

## <a name="bits-compact-server-remote-management"></a><span data-ttu-id="834d7-135">Administración remota del servidor BITS compacto</span><span class="sxs-lookup"><span data-stu-id="834d7-135">BITS Compact Server Remote Management</span></span>

<span data-ttu-id="834d7-136">El servidor BITS compacto con administración remota de BITS permite realizar transferencias de archivos remotas más seguras.</span><span class="sxs-lookup"><span data-stu-id="834d7-136">The BITS Compact Server with BITS Remote Management enables more secure remote file transfers.</span></span> <span data-ttu-id="834d7-137">La administración remota de BITS usa un proveedor de Instrumental de administración de Windows (WMI) para permitir que un administrador del sistema o una aplicación de controlador cree de forma remota trabajos de transferencia de BITS en los clientes y publique archivos para hospedarlos en el servidor BITS compacto.</span><span class="sxs-lookup"><span data-stu-id="834d7-137">BITS Remote Management uses a Windows Management Instrumentation (WMI) provider to let a system administrator or a controller application remotely create BITS transfer jobs on the clients and to publish files for hosting on the BITS Compact Server.</span></span> <span data-ttu-id="834d7-138">El proveedor de BITS también se puede usar para permitir que una aplicación use de forma remota el cliente de BITS junto con el servidor BITS compacto para transferir archivos de un equipo remoto a otro equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="834d7-138">The BITS provider can also be used to enable an application to remotely use the BITS client in conjunction with the BITS Compact Server to transfer files from one remote computer to another remote computer.</span></span>

<span data-ttu-id="834d7-139">Para obtener más información, vea la documentación del [proveedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="834d7-139">For more information, see the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="834d7-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="834d7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="834d7-141">Proveedor BITS</span><span class="sxs-lookup"><span data-stu-id="834d7-141">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 