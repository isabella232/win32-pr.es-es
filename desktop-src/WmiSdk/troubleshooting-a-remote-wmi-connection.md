---
description: En las secciones siguientes se describen los problemas comunes que pueden tener los desarrolladores con la creación de una conexión WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Solución de problemas de una conexión WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696785"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a><span data-ttu-id="8918f-103">Solución de problemas de una conexión WMI remota</span><span class="sxs-lookup"><span data-stu-id="8918f-103">Troubleshooting a Remote WMI Connection</span></span>

<span data-ttu-id="8918f-104">En las secciones siguientes se describen los problemas comunes que pueden tener los desarrolladores con la creación de una conexión WMI remota.</span><span class="sxs-lookup"><span data-stu-id="8918f-104">The following sections describe common issues developers may have with creating a remote WMI connection.</span></span>

<span data-ttu-id="8918f-105">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="8918f-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="8918f-106">Acceso a DCOM denegado</span><span class="sxs-lookup"><span data-stu-id="8918f-106">DCOM Access Denied</span></span>](#dcom-access-denied)
-   [<span data-ttu-id="8918f-107">Error de conexión</span><span class="sxs-lookup"><span data-stu-id="8918f-107">Failure to Connect</span></span>](#failure-to-connect)
-   [<span data-ttu-id="8918f-108">Se agotó el tiempo de espera de la conexión WMI</span><span class="sxs-lookup"><span data-stu-id="8918f-108">WMI Connection Timed Out</span></span>](#wmi-connection-timed-out)
-   [<span data-ttu-id="8918f-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8918f-109">Related topics</span></span>](#related-topics)

## <a name="dcom-access-denied"></a><span data-ttu-id="8918f-110">Acceso a DCOM denegado</span><span class="sxs-lookup"><span data-stu-id="8918f-110">DCOM Access Denied</span></span>

<dl> <dt>

<span data-ttu-id="8918f-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Manejo</span><span class="sxs-lookup"><span data-stu-id="8918f-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="8918f-112">no se pudo realizar la conexión con el error "acceso a DCOM denegado", junto con el valor decimal-2147024891 o Hex value0x80070005.</span><span class="sxs-lookup"><span data-stu-id="8918f-112">your connection failed with the error "DCOM Access Denied", along with the decimal value -2147024891 or hex value0x80070005.</span></span>

</dd> <dt>

<span data-ttu-id="8918f-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Publicación</span><span class="sxs-lookup"><span data-stu-id="8918f-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="8918f-114">Es posible que DCOM no esté configurado para permitir una conexión WMI.</span><span class="sxs-lookup"><span data-stu-id="8918f-114">DCOM may not be configured to allow a WMI connection.</span></span>

</dd> <dt>

<span data-ttu-id="8918f-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Traducción</span><span class="sxs-lookup"><span data-stu-id="8918f-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="8918f-116">Puede configurar DCOM para WMI mediante la utilidad de configuración DCOM (**DCOMCnfg.exe**) que se encuentra en **herramientas administrativas** del **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="8918f-116">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="8918f-117">Esta utilidad expone la configuración que permite a determinados usuarios conectarse al equipo de forma remota a través de DCOM.</span><span class="sxs-lookup"><span data-stu-id="8918f-117">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="8918f-118">Los miembros del grupo administradores pueden conectarse remotamente al equipo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8918f-118">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="8918f-119">Con esta utilidad puede establecer la seguridad para iniciar, tener acceso y configurar el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="8918f-119">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="8918f-120">Para obtener más información, consulte [protección de una conexión WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8918f-120">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

</dd> </dl>

## <a name="failure-to-connect"></a><span data-ttu-id="8918f-121">Error de conexión</span><span class="sxs-lookup"><span data-stu-id="8918f-121">Failure to Connect</span></span>

<dl> <dt>

<span data-ttu-id="8918f-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Manejo</span><span class="sxs-lookup"><span data-stu-id="8918f-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="8918f-123">No se puede conectar a WMI en un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="8918f-123">You cannot connect to WMI on a remote system.</span></span>

</dd> <dt>

<span data-ttu-id="8918f-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Publicación</span><span class="sxs-lookup"><span data-stu-id="8918f-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="8918f-125">Es posible que esté intentando conectarse a un sistema que no es compatible con WMI.</span><span class="sxs-lookup"><span data-stu-id="8918f-125">You may be trying to connect to a system that does not support WMI.</span></span> <span data-ttu-id="8918f-126">No se admiten las siguientes conexiones entre versiones de sistema operativo:</span><span class="sxs-lookup"><span data-stu-id="8918f-126">The following connections between operating system versions are not supported:</span></span>

-   <span data-ttu-id="8918f-127">No se puede conectar a un equipo que ejecute una edición Starter, Basic o Home.</span><span class="sxs-lookup"><span data-stu-id="8918f-127">You cannot connect to a computer that is running a Starter, Basic, or Home edition.</span></span>

<span data-ttu-id="8918f-128">Como alternativa, es posible que esté intentando conectarse a un espacio de nombres que requiera una conexión cifrada, una que requiera un nivel de autenticación `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** o una **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="8918f-128">Alternately, you may be trying to connect to a namespace which requires an encrypted connection, one that requires an authentication level of `pktPrivacy`, **WbemAuthenticationLevelPktPrivacy**, or **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

</dd> <dt>

<span data-ttu-id="8918f-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Traducción</span><span class="sxs-lookup"><span data-stu-id="8918f-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="8918f-130">Para obtener más información, vea [proteger los espacios de nombres de WMI](securing-wmi-namespaces.md), [proteger los clientes y proveedores de C++](securing-c---clients-and-providers.md)o [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="8918f-130">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

</dd> </dl>

## <a name="wmi-connection-timed-out"></a><span data-ttu-id="8918f-131">Se agotó el tiempo de espera de la conexión WMI</span><span class="sxs-lookup"><span data-stu-id="8918f-131">WMI Connection Timed Out</span></span>

<dl> <dt>

<span data-ttu-id="8918f-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Manejo</span><span class="sxs-lookup"><span data-stu-id="8918f-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="8918f-133">Se agota el tiempo de espera de la conexión WMI.</span><span class="sxs-lookup"><span data-stu-id="8918f-133">Your WMI connection times out.</span></span>

</dd> <dt>

<span data-ttu-id="8918f-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Publicación</span><span class="sxs-lookup"><span data-stu-id="8918f-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="8918f-135">Debido a problemas de retraso de red, el equipo no es capaz de responder a tiempo.</span><span class="sxs-lookup"><span data-stu-id="8918f-135">Due to network lag issues, the computer is simply not able to respond in time.</span></span>

</dd> <dt>

<span data-ttu-id="8918f-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Traducción</span><span class="sxs-lookup"><span data-stu-id="8918f-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="8918f-137">Al conectarse a WMI a través de una llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), puede establecer el valor de la marca **wbemConnectFlagUseMaxWait** (scripting) o la marca WBEM de la opción **\_ \_ Connect \_ use \_ Max \_ Wait** in C++ en 128 (0x80) para imponer un tiempo de espera de dos (2) minutos en la llamada.</span><span class="sxs-lookup"><span data-stu-id="8918f-137">When connecting to WMI through a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) or [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), you can set the **wbemConnectFlagUseMaxWait** flag (scripting) or the **WBEM\_FLAG\_CONNECT\_USE\_MAX\_WAIT** in C++ value to 128 (0x80) to impose a two (2) minute time-out on the call.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8918f-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8918f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8918f-139">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="8918f-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



