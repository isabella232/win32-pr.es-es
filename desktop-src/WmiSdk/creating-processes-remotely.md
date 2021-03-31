---
description: Puede usar Win32 \_ Process. Create para ejecutar un script o una aplicación en un equipo remoto. Sin embargo, por motivos de seguridad, el proceso no puede ser interactivo. Cuando \_ se llama a Win32 Process. Create en el equipo local, el proceso puede ser interactivo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Crear procesos de forma remota mediante WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816686"
---
# <a name="creating-processes-remotely-using-wmi"></a><span data-ttu-id="fea71-105">Crear procesos de forma remota mediante WMI</span><span class="sxs-lookup"><span data-stu-id="fea71-105">Creating Processes Remotely using WMI</span></span>

<span data-ttu-id="fea71-106">Puede usar [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) para ejecutar un script o una aplicación en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="fea71-106">You can use [**Win32\_Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) to execute a script or application on a remote computer.</span></span> <span data-ttu-id="fea71-107">Sin embargo, por motivos de seguridad, el proceso no puede ser interactivo.</span><span class="sxs-lookup"><span data-stu-id="fea71-107">However, for security reasons, the process cannot be interactive.</span></span> <span data-ttu-id="fea71-108">Cuando se llama a **Win32 \_ Process. Create** en el equipo local, el proceso puede ser interactivo.</span><span class="sxs-lookup"><span data-stu-id="fea71-108">When **Win32\_Process.Create** is called on the local computer, the process can be interactive.</span></span>

> [!WARNING]
> <span data-ttu-id="fea71-109">En este tema se describe el procedimiento general para crear un proceso remoto con WMI.</span><span class="sxs-lookup"><span data-stu-id="fea71-109">This topic describes the general procedure for creating a remote process with WMI.</span></span> <span data-ttu-id="fea71-110">Si simplemente desea ejecutar un script en un sistema remoto, consulte [conexión a WMI de forma remota a partir de Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)o [conexión a WMI en un equipo remoto mediante Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="fea71-110">If you are simply looking to run a script on a remote system, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md), or [Connecting to WMI on a Remote Computer by Using Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span> <span data-ttu-id="fea71-111">Para obtener más información general sobre la comunicación remota con PowerShell, vea [ejecutar comandos remotos](https://technet.microsoft.com/library/dd819505.aspx).</span><span class="sxs-lookup"><span data-stu-id="fea71-111">For more general information on remoting with PowerShell, see [Running Remote Commands](https://technet.microsoft.com/library/dd819505.aspx).</span></span>

 

<span data-ttu-id="fea71-112">El proceso remoto no tiene ninguna interfaz de usuario, pero aparece en el **Administrador de tareas**.</span><span class="sxs-lookup"><span data-stu-id="fea71-112">The remote process has no user interface but it is listed in the **Task Manager**.</span></span> <span data-ttu-id="fea71-113">Un proceso creado localmente puede ejecutarse en cualquier cuenta si la cuenta tiene el permiso **Ejecutar método** para el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="fea71-113">A process created locally can run under any account if the account has the **Execute Method** permission for the root\\cimv2 namespace.</span></span> <span data-ttu-id="fea71-114">Un proceso creado de forma remota puede ejecutarse en cualquier cuenta si la cuenta tiene los permisos **Ejecutar método** y acceso **remoto habilitado** para la raíz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="fea71-114">A process created remotely can run under any account if the account has the **Execute Method** and **Remote Enable** permissions for root\\cimv2.</span></span> <span data-ttu-id="fea71-115">Los permisos **método Execute** y **Habilitar remoto** se establecen en control WMI en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="fea71-115">The **Execute Method** and **Remote Enable** permissions are set in WMI Control in the Control Panel.</span></span> <span data-ttu-id="fea71-116">Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="fea71-116">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

<span data-ttu-id="fea71-117">Puede usar [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) para crear un proceso interactivo de forma remota.</span><span class="sxs-lookup"><span data-stu-id="fea71-117">You can use [**Win32\_ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) to create an interactive process remotely.</span></span> <span data-ttu-id="fea71-118">Pero los procesos iniciados por **Win32 \_ ScheduledJob. Create** se ejecutan en la cuenta LocalSystem que puede conferir demasiados privilegios.</span><span class="sxs-lookup"><span data-stu-id="fea71-118">But processes started by **Win32\_ScheduledJob.Create** run under the LocalSystem account that can confer too much privilege.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fea71-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fea71-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea71-120">Protección de una conexión WMI remota</span><span class="sxs-lookup"><span data-stu-id="fea71-120">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="fea71-121">Conexión a un tercer equipo: Delegación</span><span class="sxs-lookup"><span data-stu-id="fea71-121">Connecting to a 3rd Computer-Delegation</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
