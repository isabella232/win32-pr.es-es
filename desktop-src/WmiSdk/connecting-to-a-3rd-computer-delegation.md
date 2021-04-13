---
description: Al ejecutar un script en un sistema local que obtiene datos de un sistema remoto, WMI proporciona sus credenciales al proveedor de los datos en el sistema remoto.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delegación con WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424135"
---
# <a name="delegating-with-wmi"></a><span data-ttu-id="75237-103">Delegación con WMI</span><span class="sxs-lookup"><span data-stu-id="75237-103">Delegating with WMI</span></span>

<span data-ttu-id="75237-104">Al ejecutar un script en un sistema local que obtiene datos de un sistema remoto, WMI proporciona sus credenciales al proveedor de los datos en el sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="75237-104">When you run a script on a local system that obtains data from a remote system, WMI supplies your credentials to the provider of the data on the remote system.</span></span> <span data-ttu-id="75237-105">Esto requiere solo un nivel de suplantación de **Suplantar**, porque solo se requiere un salto de red.</span><span class="sxs-lookup"><span data-stu-id="75237-105">This requires only an impersonation level of **Impersonate**, because only one network hop is required.</span></span> <span data-ttu-id="75237-106">Sin embargo, si el script se conecta a WMI en el sistema remoto e intenta abrir un archivo de registro en un sistema remoto adicional, el script producirá un error a menos que el nivel de suplantación sea **Delegate**.</span><span class="sxs-lookup"><span data-stu-id="75237-106">However, if the script connects to WMI on the remote system and attempts to open a log file on an additional remote system, then the script fails unless the impersonation level is **Delegate**.</span></span> <span data-ttu-id="75237-107">El nivel de suplantación de **delegado** es necesario para cualquier operación que implique más de un salto de red.</span><span class="sxs-lookup"><span data-stu-id="75237-107">**Delegate** impersonation level is required by any operation that involves more than one network hop.</span></span> <span data-ttu-id="75237-108">Para obtener más información sobre la seguridad de DCOM en WMI, vea establecer la seguridad del proceso de la [aplicación cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="75237-108">For more information about DCOM security in WMI, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="75237-109">Para obtener más información acerca de la conexión de un salto de red entre dos equipos, consulte [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="75237-109">For more information about a one-network hop connection between two computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="75237-110">**Para usar la delegación para conectarse a un equipo a través de otro equipo**</span><span class="sxs-lookup"><span data-stu-id="75237-110">**To use delegation to connect to a computer through another computer**</span></span>

1.  <span data-ttu-id="75237-111">Habilite la delegación en Active Directory (**Active Directory usuarios y equipos** en el **Panel de control** **tareas administrativas**) en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="75237-111">Enable delegation in Active Directory (**Active Directory Users and Computers** in **Control Panel** **Administrative Tasks**) on the domain controller.</span></span> <span data-ttu-id="75237-112">La cuenta del sistema remoto debe estar marcada como **de confianza para la delegación** y la cuenta del sistema local no debe estar marcada como la **cuenta es importante y no se puede delegar**.</span><span class="sxs-lookup"><span data-stu-id="75237-112">The account on the remote system must be marked as **Trusted for delegation** and the account on the local system must not be marked as **Account is sensitive and cannot be delegated**.</span></span> <span data-ttu-id="75237-113">el sistema local, el sistema remoto y el controlador de dominio deben ser miembros del mismo dominio o de dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="75237-113">the local system, the remote system, and the domain controller must be members of the same domain or in trusted domains.</span></span>

    <span data-ttu-id="75237-114">**Nota:**  El uso de la delegación supone un riesgo para la seguridad, ya que proporciona a los procesos que están fuera de su control directo la capacidad de usar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="75237-114">**Note**  Using delegation is a security risk because it gives processes outside of your direct control the ability to use your credentials.</span></span>

2.  <span data-ttu-id="75237-115">Modifique el código de la siguiente manera para indicar que desea usar la delegación.</span><span class="sxs-lookup"><span data-stu-id="75237-115">Modify your code in the following manner to indicate that you want to use delegation.</span></span>

    <dl> <dt>

    <span data-ttu-id="75237-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span><span class="sxs-lookup"><span data-stu-id="75237-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span></span>
    </dt> <dd>

    <span data-ttu-id="75237-117">Establezca el parámetro *-Impersonation* en el CMDLET de WMI en **Delegate**.</span><span class="sxs-lookup"><span data-stu-id="75237-117">Set the *-Impersonation* parameter on the WMI cmdlet to **Delegate**.</span></span>

    </dd> <dt>

    <span data-ttu-id="75237-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span><span class="sxs-lookup"><span data-stu-id="75237-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span></span>
    </dt> <dd>

    <span data-ttu-id="75237-119">Establezca el parámetro *impersonationLevel* en **Delegate** en la llamada a [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) o **Delegate** en la cadena de [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="75237-119">Set the *impersonationLevel* parameter to **Delegate** in the call to [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) or **Delegate** in the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="75237-120">También puede establecer la suplantación en un objeto [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="75237-120">You can also set the impersonation in a [**SWbemSecurity**](swbemsecurity.md)object.</span></span>

    </dd> <dt>

    <span data-ttu-id="75237-121"><span id="C__"></span><span id="c__"></span>C++</span><span class="sxs-lookup"><span data-stu-id="75237-121"><span id="C__"></span><span id="c__"></span>C++</span></span>
    </dt> <dd>

    <span data-ttu-id="75237-122">Establezca el parámetro de nivel de suplantación en el **\_ \_ \_ \_ delegado de nivel Imp de RPC C** en la llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="75237-122">Set the impersonation level parameter to **RPC\_C\_IMP\_LEVEL\_DELEGATE** in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="75237-123">Para obtener más información acerca de cuándo realizar estas llamadas, consulte [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="75237-123">For more information about when to make these calls, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="75237-124">Para pasar la identidad del cliente a los servidores COM remotos en C++, establezca Cloaking en la llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="75237-124">To pass the client identity to remote COM servers in C++, set cloaking in the call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="75237-125">Para obtener más información, consulte [Cloaking](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="75237-125">For more information, see [Cloaking](../com/cloaking.md).</span></span>

    </dd> </dl>

## <a name="examples"></a><span data-ttu-id="75237-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75237-126">Examples</span></span>

<span data-ttu-id="75237-127">En el ejemplo de código siguiente se muestra una cadena de moniker que establece la suplantación en **Delegate**.</span><span class="sxs-lookup"><span data-stu-id="75237-127">The following code example shows a moniker string that sets the impersonation to **Delegate**.</span></span> <span data-ttu-id="75237-128">Tenga en cuenta que la autoridad debe establecerse en Kerberos.</span><span class="sxs-lookup"><span data-stu-id="75237-128">Be aware that the authority must be set to Kerberos.</span></span>


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



<span data-ttu-id="75237-129">En el ejemplo de código siguiente se muestra cómo establecer la suplantación en **Delegate** (un valor de 4) mediante [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="75237-129">The following code example shows how to set impersonation to **Delegate** (a value of 4) using [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a><span data-ttu-id="75237-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75237-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75237-131">Protección de una conexión WMI remota</span><span class="sxs-lookup"><span data-stu-id="75237-131">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="75237-132">Crear procesos de forma remota con WMI</span><span class="sxs-lookup"><span data-stu-id="75237-132">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> </dl>

 

 
