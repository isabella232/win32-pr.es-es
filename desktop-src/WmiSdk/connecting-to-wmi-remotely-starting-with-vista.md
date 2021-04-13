---
description: La conexión a un espacio de nombres WMI en un equipo remoto puede requerir que se cambie la configuración del firewall de Windows, el control de cuentas de usuario (UAC), DCOM o el administrador de objetos de Modelo de información común (CIMOM).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configuración de una conexión WMI remota
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544846"
---
# <a name="setting-up-a-remote-wmi-connection"></a><span data-ttu-id="7f3b9-103">Configuración de una conexión WMI remota</span><span class="sxs-lookup"><span data-stu-id="7f3b9-103">Setting up a Remote WMI Connection</span></span>

<span data-ttu-id="7f3b9-104">La conexión a un espacio de nombres WMI en un equipo remoto puede requerir que se cambie la configuración del [firewall de Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), el control de [cuentas de usuario (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM o el administrador de objetos de modelo de información común (CIMOM).</span><span class="sxs-lookup"><span data-stu-id="7f3b9-104">Connecting to a WMI namespace on a remote computer may require that you change the settings for [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM, or Common Information Model Object Manager (CIMOM).</span></span>

<span data-ttu-id="7f3b9-105">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="7f3b9-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="7f3b9-106">Configuración de Firewall de Windows</span><span class="sxs-lookup"><span data-stu-id="7f3b9-106">Windows Firewall Settings</span></span>](#windows-firewall-settings)
-   [<span data-ttu-id="7f3b9-107">Configuración de Control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="7f3b9-107">User Account Control Settings</span></span>](#user-account-control-settings)
-   [<span data-ttu-id="7f3b9-108">Configuración de DCOM</span><span class="sxs-lookup"><span data-stu-id="7f3b9-108">DCOM Settings</span></span>](#dcom-settings)
-   [<span data-ttu-id="7f3b9-109">Configuración de CIMOM</span><span class="sxs-lookup"><span data-stu-id="7f3b9-109">CIMOM Settings</span></span>](#cimom-settings)
-   [<span data-ttu-id="7f3b9-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f3b9-110">Related topics</span></span>](#related-topics)

## <a name="windows-firewall-settings"></a><span data-ttu-id="7f3b9-111">Configuración de Windows Firewall</span><span class="sxs-lookup"><span data-stu-id="7f3b9-111">Windows Firewall Settings</span></span>

<span data-ttu-id="7f3b9-112">La configuración de WMI para la configuración de Firewall de Windows solo permite conexiones WMI, en lugar de otras aplicaciones DCOM.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-112">WMI settings for Windows Firewall settings enable only WMI connections, rather than other DCOM applications as well.</span></span>

<span data-ttu-id="7f3b9-113">Debe establecerse una excepción en el firewall para WMI en el equipo de destino remoto.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-113">An exception must be set in the firewall for WMI on the remote target computer.</span></span> <span data-ttu-id="7f3b9-114">La excepción para WMI permite a WMI recibir conexiones remotas y devoluciones de llamada asincrónicas para Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-114">The exception for WMI allows WMI to receive remote connections and asynchronous callbacks to Unsecapp.exe.</span></span> <span data-ttu-id="7f3b9-115">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="7f3b9-115">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="7f3b9-116">Si una aplicación cliente crea su propio receptor, ese receptor debe agregarse explícitamente a las excepciones de Firewall para permitir que las devoluciones de llamada se realicen correctamente.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-116">If a client application creates its own sink, that sink must be explicitly added to the firewall exceptions to allow callbacks to succeed.</span></span>

<span data-ttu-id="7f3b9-117">La excepción para WMI también funciona si se ha iniciado WMI con un puerto fijo, mediante el comando **WinMgmt/standalonehost** .</span><span class="sxs-lookup"><span data-stu-id="7f3b9-117">The exception for WMI also works if WMI has been started with a fixed port, using the **winmgmt /standalonehost** command.</span></span> <span data-ttu-id="7f3b9-118">Para obtener más información, consulte [configuración de un puerto fijo para WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7f3b9-118">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="7f3b9-119">Puede habilitar o deshabilitar el tráfico WMI a través de la interfaz de usuario del firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-119">You can enable or disable WMI traffic through the Windows Firewall UI.</span></span>

<span data-ttu-id="7f3b9-120">**Para habilitar o deshabilitar el tráfico WMI mediante la interfaz de usuario del firewall**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-120">**To enable or disable WMI traffic using firewall UI**</span></span>

1.  <span data-ttu-id="7f3b9-121">En el **Panel de control**, haga clic en **seguridad** y, a continuación, en **firewall de Windows**.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-121">In the **Control Panel**, click **Security** and then click **Windows Firewall**.</span></span>
2.  <span data-ttu-id="7f3b9-122">Haga clic en **Cambiar configuración** y, a continuación, haga clic en la pestaña **excepciones** .</span><span class="sxs-lookup"><span data-stu-id="7f3b9-122">Click **Change Settings** and then click the **Exceptions** tab.</span></span>
3.  <span data-ttu-id="7f3b9-123">En la ventana excepciones, active la casilla de **instrumental de administración de Windows (WMI)** para habilitar el tráfico WMI a través del firewall.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-123">In the Exceptions window, select the check box for **Windows Management Instrumentation (WMI)** to enable WMI traffic through the firewall.</span></span> <span data-ttu-id="7f3b9-124">Para deshabilitar el tráfico WMI, desactive la casilla.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-124">To disable WMI traffic, clear the check box.</span></span>

<span data-ttu-id="7f3b9-125">Puede habilitar o deshabilitar el tráfico WMI a través del firewall en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-125">You can enable or disable WMI traffic through the firewall at the command prompt.</span></span>

<span data-ttu-id="7f3b9-126">**Para habilitar o deshabilitar el tráfico WMI en el símbolo del sistema mediante el grupo de reglas WMI**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-126">**To enable or disable WMI traffic at command prompt using WMI rule group**</span></span>

-   <span data-ttu-id="7f3b9-127">Use los comandos siguientes en un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-127">Use the following commands at a command prompt.</span></span> <span data-ttu-id="7f3b9-128">Escriba lo siguiente para habilitar el tráfico WMI a través del firewall.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-128">Type the following to enable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="7f3b9-129">**netsh advfirewall firewall set Rule Group = "instrumental de administración de Windows (WMI)" New enable = Yes**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-129">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**</span></span>

    <span data-ttu-id="7f3b9-130">Escriba el siguiente comando para deshabilitar el tráfico WMI a través del firewall.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-130">Type the following command to disable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="7f3b9-131">**netsh advfirewall firewall set Rule Group = "instrumental de administración de Windows (WMI)" New enable = no**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-131">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**</span></span>

<span data-ttu-id="7f3b9-132">En lugar de usar el comando de grupo de reglas de WMI único, también puede usar comandos individuales para cada uno de los servicios DCOM, WMI y Sink.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-132">Rather than using the single WMI rule group command, you also can use individual commands for each of the DCOM, WMI service, and sink.</span></span>

<span data-ttu-id="7f3b9-133">**Para habilitar el tráfico WMI mediante reglas independientes para DCOM, WMI, receptor de devoluciones de llamada y conexiones salientes**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-133">**To enable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="7f3b9-134">Para establecer una excepción de Firewall para el puerto DCOM 135, use el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-134">To establish a firewall exception for DCOM port 135, use the following command.</span></span>

    <span data-ttu-id="7f3b9-135">**netsh advfirewall Firewall Add Rule Dir = in name = "DCOM" Program =% SystemRoot% \\ system32 \\svchost.exe Service = RPCSS Action = allow Protocol = TCP localport = 135**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-135">**netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot%\\system32\\svchost.exe service=rpcss action=allow protocol=TCP localport=135**</span></span>

2.  <span data-ttu-id="7f3b9-136">Para establecer una excepción de Firewall para el servicio WMI, use el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-136">To establish a firewall exception for the WMI service, use the following command.</span></span>

    <span data-ttu-id="7f3b9-137">**netsh advfirewall Firewall Add Rule Dir = in name = "WMI" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt Action = allow Protocol = TCP localport = any**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-137">**netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot%\\system32\\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**</span></span>

3.  <span data-ttu-id="7f3b9-138">Para establecer una excepción de Firewall para el receptor que recibe las devoluciones de llamada desde un equipo remoto, use el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-138">To establish a firewall exception for the sink that receives callbacks from a remote computer, use the following command.</span></span>

    <span data-ttu-id="7f3b9-139">**netsh advfirewall Firewall Add Rule Dir = in name = "UnsecApp" Program =% SystemRoot% \\ system32 \\ WBEM \\unsecapp.exe Action = allow**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-139">**netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot%\\system32\\wbem\\unsecapp.exe action=allow**</span></span>

4.  <span data-ttu-id="7f3b9-140">Para establecer una excepción de Firewall para las conexiones salientes a un equipo remoto con el que el equipo local se comunica de forma asincrónica, use el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-140">To establish a firewall exception for outgoing connections to a remote computer that the local computer is communicating with asynchronously, use the following command.</span></span>

    <span data-ttu-id="7f3b9-141">**netsh advfirewall Firewall Add Rule dir = out name = "WMI \_ out" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt Action = allow Protocol = TCP localport = any**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-141">**netsh advfirewall firewall add rule dir=out name ="WMI\_OUT" program=%systemroot%\\system32\\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**</span></span>

<span data-ttu-id="7f3b9-142">Para deshabilitar las excepciones de Firewall por separado, use los comandos siguientes.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-142">To disable the firewall exceptions separately, use the following commands.</span></span>

<span data-ttu-id="7f3b9-143">**Para deshabilitar el tráfico WMI mediante reglas independientes para DCOM, WMI, receptor de devoluciones de llamada y conexiones salientes**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-143">**To disable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="7f3b9-144">Para deshabilitar la excepción DCOM.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-144">To disable the DCOM exception.</span></span>

    <span data-ttu-id="7f3b9-145">**netsh advfirewall Firewall Delete Rule name = "DCOM"**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-145">**netsh advfirewall firewall delete rule name="DCOM"**</span></span>

2.  <span data-ttu-id="7f3b9-146">Para deshabilitar la excepción de servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-146">To disable the WMI service exception.</span></span>

    <span data-ttu-id="7f3b9-147">**netsh advfirewall Firewall Delete Rule name = "WMI"**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-147">**netsh advfirewall firewall delete rule name="WMI"**</span></span>

3.  <span data-ttu-id="7f3b9-148">Para deshabilitar la excepción de receptor.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-148">To disable the sink exception.</span></span>

    <span data-ttu-id="7f3b9-149">**netsh advfirewall Firewall Delete Rule name = "UnsecApp"**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-149">**netsh advfirewall firewall delete rule name="UnsecApp"**</span></span>

4.  <span data-ttu-id="7f3b9-150">Para deshabilitar la excepción de salida.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-150">To disable the outgoing exception.</span></span>

    <span data-ttu-id="7f3b9-151">**netsh advfirewall Firewall Delete Rule name = "WMI \_ out"**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-151">**netsh advfirewall firewall delete rule name="WMI\_OUT"**</span></span>

## <a name="user-account-control-settings"></a><span data-ttu-id="7f3b9-152">Configuración de Control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="7f3b9-152">User Account Control Settings</span></span>

<span data-ttu-id="7f3b9-153">El filtrado de tokens de acceso de control de cuentas de usuario (UAC) puede afectar a las operaciones permitidas en los espacios de nombres WMI o a los datos que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-153">User Account Control (UAC) access-token filtering can affect which operations are allowed in WMI namespaces or what data is returned.</span></span> <span data-ttu-id="7f3b9-154">En UAC, todas las cuentas del grupo de administradores locales se ejecutan con un [*token de acceso*](/windows/desktop/SecGloss/a-gly)de usuario estándar, también conocido como filtrado de tokens de acceso de UAC.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-154">Under UAC, all accounts in the local Administrators group run with a standard user [*access token*](/windows/desktop/SecGloss/a-gly), also known as UAC access-token filtering.</span></span> <span data-ttu-id="7f3b9-155">Una cuenta de administrador puede ejecutar un script con privilegios elevados, "ejecutar como administrador".</span><span class="sxs-lookup"><span data-stu-id="7f3b9-155">An administrator account can run a script with an elevated privilege—"Run as Administrator".</span></span>

<span data-ttu-id="7f3b9-156">Cuando no se conecta a la cuenta predefinida de administrador, UAC afecta a las conexiones a un equipo remoto de forma distinta en función de si los dos equipos están en un dominio o un grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-156">When you are not connecting to the built-in Administrator account, UAC affects connections to a remote computer differently depending on whether the two computers are in a domain or a workgroup.</span></span> <span data-ttu-id="7f3b9-157">Para obtener más información sobre UAC y las conexiones remotas, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7f3b9-157">For more information about UAC and remote connections, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="dcom-settings"></a><span data-ttu-id="7f3b9-158">Configuración de DCOM</span><span class="sxs-lookup"><span data-stu-id="7f3b9-158">DCOM Settings</span></span>

<span data-ttu-id="7f3b9-159">Para obtener más información sobre la configuración de DCOM, consulte [protección de una conexión WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7f3b9-159">For more information on DCOM settings, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span> <span data-ttu-id="7f3b9-160">Sin embargo, UAC afecta a las conexiones para las cuentas de usuario que no son de dominio.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-160">However, UAC affects connections for nondomain user accounts.</span></span> <span data-ttu-id="7f3b9-161">Si se conecta a un equipo remoto mediante una cuenta de usuario que no es de dominio incluida en el grupo de administradores local del equipo remoto, debe conceder explícitamente derechos de acceso remoto DCOM, activación e inicio a la cuenta.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-161">If you connect to a remote computer using a nondomain user account included in the local Administrators group of the remote computer, then you must explicitly grant remote DCOM access, activation, and launch rights to the account.</span></span>

## <a name="cimom-settings"></a><span data-ttu-id="7f3b9-162">Configuración de CIMOM</span><span class="sxs-lookup"><span data-stu-id="7f3b9-162">CIMOM Settings</span></span>

<span data-ttu-id="7f3b9-163">La configuración de CIMOM debe actualizarse si la conexión remota se realiza entre equipos que no tienen una relación de confianza. de lo contrario, se producirá un error en una conexión asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-163">The CIMOM settings need to be updated if the remote connection is between computers that do not have a trust relationship; otherwise, an asynchronous connection will fail.</span></span> <span data-ttu-id="7f3b9-164">Esta configuración no se debe modificar para los equipos que se encuentra en el mismo dominio o en dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-164">This setting should not be modified for computers in the same domain or in trusted domains.</span></span>

<span data-ttu-id="7f3b9-165">La siguiente entrada del registro debe modificarse para permitir las devoluciones de llamada anónimas:</span><span class="sxs-lookup"><span data-stu-id="7f3b9-165">The following registry entry needs to be modified to allow anonymous callbacks:</span></span>

<span data-ttu-id="7f3b9-166">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**</span><span class="sxs-lookup"><span data-stu-id="7f3b9-166">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**AllowAnonymousCallback**</span></span><dl> <dt>

               Data type
</dt> <dd>               <span data-ttu-id="7f3b9-167">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7f3b9-167">REG\_DWORD</span></span></dd> </dl>

<span data-ttu-id="7f3b9-168">Si el valor de **AllowAnonymousCallback** se establece en 0, el servicio WMI impide las devoluciones de llamada anónimas al cliente.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-168">If the **AllowAnonymousCallback** value is set to 0, the WMI service prevents anonymous callbacks to the client.</span></span> <span data-ttu-id="7f3b9-169">Si el valor se establece en 1, el servicio WMI permite devoluciones de llamada anónimas al cliente.</span><span class="sxs-lookup"><span data-stu-id="7f3b9-169">If the value is set to 1, the WMI service allows anonymous callbacks to the client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f3b9-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f3b9-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f3b9-171">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="7f3b9-171">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
