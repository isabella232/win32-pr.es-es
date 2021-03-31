---
description: Los scripts de WMI pueden condensar muchos de los pasos necesarios en un programa de C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Conectarse a WMI con VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911514"
---
# <a name="connecting-to-wmi-with-vbscript"></a><span data-ttu-id="55701-103">Conectarse a WMI con VBScript</span><span class="sxs-lookup"><span data-stu-id="55701-103">Connecting to WMI with VBScript</span></span>

<span data-ttu-id="55701-104">Los scripts de WMI pueden condensar muchos de los pasos necesarios en un programa de C++.</span><span class="sxs-lookup"><span data-stu-id="55701-104">WMI scripts can condense many of the steps required in a C++ program.</span></span> <span data-ttu-id="55701-105">Pueden conectarse a WMI, no solo a través de un objeto [**SWbemLocator**](swbemlocator.md) , sino también a través del moniker "winmgmts:".</span><span class="sxs-lookup"><span data-stu-id="55701-105">They can connect to WMI, not only through an [**SWbemLocator**](swbemlocator.md) object, but also through the moniker "winmgmts:".</span></span> <span data-ttu-id="55701-106">Un moniker es un nombre corto que ubica un espacio de nombres, una clase o una instancia en WMI.</span><span class="sxs-lookup"><span data-stu-id="55701-106">A moniker is a short name that locates a namespace, class, or instance in WMI.</span></span> <span data-ttu-id="55701-107">El nombre "winmgmts:" es el moniker de WMI que indica a Windows Script Host que use los objetos WMI, se conecta al espacio de nombres predeterminado y obtiene un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="55701-107">The name "winmgmts:" is the WMI moniker that tells the Windows Script Host to use the WMI objects, connects to the default namespace, and obtains an [**SWbemServices**](swbemservices.md) object.</span></span> <span data-ttu-id="55701-108">Otra información de conexión, como un nivel de suplantación o una clase o instancia específica, aparece en la cadena que sigue al nombre del moniker.</span><span class="sxs-lookup"><span data-stu-id="55701-108">Other connection information, such as an impersonation level or a specific class or instance, appears in the string following the moniker name.</span></span> <span data-ttu-id="55701-109">Puede usar monikers en llamadas que creen u obtengan objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="55701-109">You can use monikers in calls that either create or get WMI objects.</span></span> <span data-ttu-id="55701-110">Para obtener más información, vea [crear una cadena de moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="55701-110">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

<span data-ttu-id="55701-111">En el procedimiento siguiente se describe cómo conectarse a WMI mediante **SWbemLocator**.</span><span class="sxs-lookup"><span data-stu-id="55701-111">The following procedure describes how to connect to WMI using **SWbemLocator**.</span></span>

<span data-ttu-id="55701-112">**Para conectarse a WMI mediante SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="55701-112">**To connect to WMI using SWbemLocator**</span></span>

1.  <span data-ttu-id="55701-113">Recupere un objeto localizador con una llamada a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55701-113">Retrieve a locator object with a call to [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  <span data-ttu-id="55701-114">Inicie sesión en el espacio de nombres mediante una llamada al método [**ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="55701-114">Log on to the namespace using a call to the [**ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    <span data-ttu-id="55701-115">Si no especifica un equipo en la llamada a [**ConnectServer**](swbemlocator-connectserver.md), WMI se conectará al equipo local.</span><span class="sxs-lookup"><span data-stu-id="55701-115">If you do not specify a computer in the call to [**ConnectServer**](swbemlocator-connectserver.md), then WMI connects to the local computer.</span></span> <span data-ttu-id="55701-116">Si no especifica un espacio de nombres, WMI se conecta al espacio de nombres especificado en la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="55701-116">If you do not specify a namespace, then WMI connects to the namespace specified in the registry key.</span></span>

    <span data-ttu-id="55701-117">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **scripting** \\ **default namespace**</span><span class="sxs-lookup"><span data-stu-id="55701-117">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**</span></span>

    <span data-ttu-id="55701-118">El espacio de nombres predeterminado es la \\ raíz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="55701-118">The default namespace is \\root\\cimv2.</span></span> <span data-ttu-id="55701-119">Para obtener más información sobre los espacios de nombres, vea [Crear jerarquías en WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="55701-119">For more information about namespaces, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

3.  <span data-ttu-id="55701-120">Establezca el nivel de suplantación con una llamada al método [**SWbemServices. \_ Security**](swbemservices-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="55701-120">Set the impersonation level with a call to the [**SWbemServices.Security\_**](swbemservices-security-.md) method.</span></span>

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    <span data-ttu-id="55701-121">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="55701-121">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

4.  <span data-ttu-id="55701-122">Implemente el propósito del script.</span><span class="sxs-lookup"><span data-stu-id="55701-122">Implement the purpose of your script.</span></span>

    <span data-ttu-id="55701-123">WMI expone una variedad de objetos de scripting que usan para tener acceso a los datos de la red y manipularlos.</span><span class="sxs-lookup"><span data-stu-id="55701-123">WMI exposes a variety of scripting objects that use to access and manipulate data across your network.</span></span> <span data-ttu-id="55701-124">Para obtener más información, consulte [manipular la información de clase e instancia](manipulating-class-and-instance-information.md) y la [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="55701-124">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

<span data-ttu-id="55701-125">En el procedimiento siguiente se describe cómo conectarse a WMI y recuperar un objeto con un moniker.</span><span class="sxs-lookup"><span data-stu-id="55701-125">The following procedure describes how to connect to WMI and retrieve an object using a moniker.</span></span>

<span data-ttu-id="55701-126">**Para conectarse a WMI y recuperar un objeto con un moniker**</span><span class="sxs-lookup"><span data-stu-id="55701-126">**To connect to WMI and retrieve an object using a moniker**</span></span>

1.  <span data-ttu-id="55701-127">Llame a [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) con un moniker en el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="55701-127">Call [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) with a moniker in the input parameter.</span></span>

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    <span data-ttu-id="55701-128">Moiniker contiene una serie de elementos que puede usar para conectarse a WMI:</span><span class="sxs-lookup"><span data-stu-id="55701-128">The moiniker contains a number of elements that you can use to connect to WMI:</span></span>

    -   <span data-ttu-id="55701-129">"Winmgmts:" indica a WSH que use los [objetos de API de scripting](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="55701-129">The "winmgmts:" tells WSH to use [Scripting API objects](scripting-api-objects.md).</span></span> <span data-ttu-id="55701-130">En este ejemplo concreto, WSH sabrá que debe devolver un SWbemObject que describa el primer scheduledJob Win32 del \_ sistema.</span><span class="sxs-lookup"><span data-stu-id="55701-130">In this particular example, the WSH will know that it should return an SWbemObject that describes the first Win32\_scheduledJob on the system.</span></span> <span data-ttu-id="55701-131">Otros posibles objetos que se van a devolver serían un objeto SWbemCollection o [**SWbemServices**](swbemservices.md) , en función del moniker descrito.</span><span class="sxs-lookup"><span data-stu-id="55701-131">Other possible objects to return would be an SWbemCollection or an [**SWbemServices**](swbemservices.md) object, depending on what the moniker described.</span></span>

    -   <span data-ttu-id="55701-132">Opcionalmente, puede establecer los niveles de seguridad de la conexión.</span><span class="sxs-lookup"><span data-stu-id="55701-132">You can optionally set the security levels for the connection.</span></span> <span data-ttu-id="55701-133">Sin embargo, tenga en cuenta que no puede establecer la información de nombre y contraseña en un moniker.</span><span class="sxs-lookup"><span data-stu-id="55701-133">Note that you cannot set name and password information in a moniker, however.</span></span> <span data-ttu-id="55701-134">Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="55701-134">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    -   <span data-ttu-id="55701-135">Opcionalmente, puede definir la ruta de acceso al objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="55701-135">You can optionally define the path to the WMI object.</span></span> <span data-ttu-id="55701-136">Esto incluye el equipo local o remoto, el espacio de nombres, así como el nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="55701-136">This includes either the local or remote computer, the namespace, as well as the name of the class.</span></span> <span data-ttu-id="55701-137">Para obtener más información acerca del uso de la expresión [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) de VBScript en scripts de WMI, vea [crear una instancia](creating-an-instance.md) y [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="55701-137">For more information about using the VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI scripts, see [Creating an Instance](creating-an-instance.md) and [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="55701-138">En lugar de recuperar un único elemento o colección, también puede optar por recuperar el objeto [**SWbemServices**](swbemservices.md) (como se describe en el ejemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="55701-138">Instead of retrieving a single item or collection, you can also choose to retrieve the [**SWbemServices**](swbemservices.md) object (as described in the previous example).</span></span> <span data-ttu-id="55701-139">Después, puede llamar a consultas adicionales en el objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="55701-139">Afterwards, you can then call additional queries on the returned object.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    <span data-ttu-id="55701-140">En el ejemplo anterior, Impersonate o impersonationLevel = 3 es el nivel de seguridad de proceso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="55701-140">In the previous example, impersonate, or impersonationLevel=3, is the default process security level.</span></span> <span data-ttu-id="55701-141">En el ejemplo siguiente, no es necesario especificar este nivel de seguridad del proceso a menos que necesite cambiar la seguridad del proceso a **Delegate**.</span><span class="sxs-lookup"><span data-stu-id="55701-141">In the following example, it is not necessary to specify this process security level unless you need to change the process security to **delegate**.</span></span> <span data-ttu-id="55701-142">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="55701-142">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55701-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55701-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55701-144">Scripting en WMI</span><span class="sxs-lookup"><span data-stu-id="55701-144">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
