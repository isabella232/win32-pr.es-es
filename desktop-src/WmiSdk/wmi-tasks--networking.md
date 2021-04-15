---
description: Las tareas de WMI para redes administran y obtienen información acerca de las conexiones y las direcciones IP o MAC. Para ver otros ejemplos, vea el ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: 25da32c3-34bf-4c88-9b09-ff371f2cf8db
ms.tgt_platform: multiple
title: 'Tareas de WMI: redes'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31e8346a064fe2f6c7ab624897be8e789474f7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715821"
---
# <a name="wmi-tasks-networking"></a><span data-ttu-id="b4f7f-104">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="b4f7f-104">WMI Tasks: Networking</span></span>

<span data-ttu-id="b4f7f-105">Las tareas de WMI para redes administran y obtienen información acerca de las conexiones y las direcciones IP o MAC.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-105">WMI tasks for networking manage and obtain information about connections and IP or MAC addresses.</span></span> <span data-ttu-id="b4f7f-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="b4f7f-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="b4f7f-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b4f7f-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="b4f7f-109">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="b4f7f-110">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="b4f7f-110">**To run a script**</span></span>

1.  <span data-ttu-id="b4f7f-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="b4f7f-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="b4f7f-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="b4f7f-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="b4f7f-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="b4f7f-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="b4f7f-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="b4f7f-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="b4f7f-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="b4f7f-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="b4f7f-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="b4f7f-121">How do I...</span></span></th>
<th><span data-ttu-id="b4f7f-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="b4f7f-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4f7f-123">... ¿deshabilitar una conexión de red mediante WMI?</span><span class="sxs-lookup"><span data-stu-id="b4f7f-123">...disable a network connection using WMI?</span></span></td>
<td><span data-ttu-id="b4f7f-124">Si usa DHCP, use el <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> para liberar la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-124">If you are using DHCP, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> and the <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> method to release the IP address.</span></span> <span data-ttu-id="b4f7f-125">Si no usa DHCP, no puede usar WMI para deshabilitar una conexión de red.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-125">If you are not using DHCP, you cannot use WMI to disable a network connection.</span></span> <span data-ttu-id="b4f7f-126">Para volver a habilitar la conexión de red, use <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard. RenewDHCPLease</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-126">To re-enable the network connection, use <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard.RenewDHCPLease</strong></a>.</span></span> <span data-ttu-id="b4f7f-127">También puede liberar o renovar todas las concesiones DHCP mediante los métodos <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> y <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-127">You can also release or renew all of the DHCP leases using the <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> and <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> methods.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-128">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetCards = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration &quot; _
        & &quot;Where IPEnabled = True&quot;)
For Each objNetCard in colNetCards
    objNetCard.ReleaseDHCPLease()
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4f7f-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$net = Get-WMIObject -class Win32_NetworkAdapterConfiguration -ComputerName $computer
$netenabled = $net | where {$_.IPenabled}
foreach ($NetCard in $netenabled) {
    &quot;Releasing lease on: {0}&quot; -f $netcard.caption
 $netcard.ReleaseDHCPLease()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f7f-130">... ¿deshabilitar o habilitar una NIC?</span><span class="sxs-lookup"><span data-stu-id="b4f7f-130">...disable or enable a NIC?</span></span></td>
<td><p><span data-ttu-id="b4f7f-131">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> y los métodos <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Disable</strong></a> o <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>enable</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Disable</strong></a> or <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>Enable</strong></a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f7f-132">... ¿determinar qué dirección IP se ha asignado a una conexión de red determinada?</span><span class="sxs-lookup"><span data-stu-id="b4f7f-132">...determine which IP address has been assigned to a given network connection?</span></span></td>
<td><p><span data-ttu-id="b4f7f-133">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> y la propiedad <strong>NetConnectionID</strong> para determinar la dirección Mac de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <strong>NetConnectionID</strong> property to determine the MAC address of the network connection.</span></span> <span data-ttu-id="b4f7f-134">A continuación, use la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> para buscar la dirección IP asociada a la dirección Mac.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-134">Then, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class to find the IP address associated with the MAC address.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-135">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection 2&#39;&quot;)

For Each objItem in colItems
    strMACAddress = objItem.MACAddress
Next

Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration&quot;)

For Each objItem in colItems
    If objItem.MACAddress = strMACAddress Then
        For Each strIPAddress in objItem.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-136">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNics = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection&#39;&quot;)
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      (&quot;ASSOCIATORS OF &quot; _
          & &quot;{Win32_NetworkAdapter.DeviceID=&#39;&quot; & _
      objNic.DeviceID & &quot;&#39;}&quot; & _
      &quot; WHERE AssocClass=Win32_NetworkAdapterSetting&quot;)
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f7f-137">... determinar la dirección MAC de un adaptador de red</span><span class="sxs-lookup"><span data-stu-id="b4f7f-137">...determine the MAC address of a network adapter?</span></span></td>
<td><p><span data-ttu-id="b4f7f-138">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> y compruebe el valor de la propiedad <strong>MacAddress</strong> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>MACAddress</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f7f-139">... determinar la dirección IP de un equipo</span><span class="sxs-lookup"><span data-stu-id="b4f7f-139">...determine the IP address of a computer?</span></span></td>
<td><p><span data-ttu-id="b4f7f-140">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> y compruebe el valor de la propiedad <strong>IPAddress</strong> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>IPAddress</strong> property.</span></span> <span data-ttu-id="b4f7f-141">Esto se devuelve como una matriz, por lo que debe usar un bucle For-Each para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-141">This is returned as an array, so use a For-Each loop to get the value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-142">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration &quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
            to UBound(IPConfig.IPAddress)
                WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4f7f-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$IPconfigset = Get-WmiObject Win32_NetworkAdapterConfiguration
  
# Iterate and get IP address
$count = 0
foreach ($IPConfig in $IPConfigSet) {
   if ($Ipconfig.IPaddress) {
      foreach ($addr in $Ipconfig.Ipaddress) {
   &quot;IP Address   : {0}&quot; -f  $addr;
   $count++ 
   }
   }
}
if ($count -eq 0) {&quot;No IP addresses found&quot;}
else {&quot;$Count IP addresses found on this system&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f7f-144">...configque un equipo empiece a obtener su dirección IP a través de DHCP?</span><span class="sxs-lookup"><span data-stu-id="b4f7f-144">...configure a computer to start getting its IP address through DHCP?</span></span></td>
<td><p><span data-ttu-id="b4f7f-145">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-146">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-146">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
 
For Each objNetAdapter In colNetAdapters
    errEnable = objNetAdapter.EnableDHCP()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f7f-147">... ¿asignar un equipo una dirección IP estática?</span><span class="sxs-lookup"><span data-stu-id="b4f7f-147">...assign a computer a static IP address?</span></span></td>
<td><p><span data-ttu-id="b4f7f-148">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-148">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-149">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-149">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
strIPAddress = Array(&quot;192.168.1.141&quot;)
strSubnetMask = Array(&quot;255.255.255.0&quot;)
strGateway = Array(&quot;192.168.1.100&quot;)
strGatewayMetric = Array(1)
 
For Each objNetAdapter in colNetAdapters
    errEnable = objNetAdapter.EnableStatic( _
        strIPAddress, strSubnetMask)
    errGateways = objNetAdapter.SetGateways(_
        strGateway, strGatewaymetric)
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f7f-150">... ¿desea obtener información acerca de los adaptadores de red sin recuperar también información sobre aspectos como conexiones RAS y VPN?</span><span class="sxs-lookup"><span data-stu-id="b4f7f-150">...get information about network adapters without also retrieving information about things like RAS and VPN connections?</span></span></td>
<td><p><span data-ttu-id="b4f7f-151">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class.</span></span> <span data-ttu-id="b4f7f-152">En la consulta <a href="querying-with-wql.md">WQL</a> , use esta cláusula: Where <strong>IPEnabled</strong>  =  <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-152">In your <a href="querying-with-wql.md">WQL</a> query, use this clause: Where <strong>IPEnabled</strong> = <strong>True</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-153">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-153">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration&quot; _
        & &quot; where IPEnabled=TRUE&quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
        to UBound(IPConfig.IPAddress)
            WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f7f-154">... ¿hacer ping a un equipo sin utilizar Ping.exe?</span><span class="sxs-lookup"><span data-stu-id="b4f7f-154">...ping a computer without using Ping.exe?</span></span></td>
<td><p><span data-ttu-id="b4f7f-155">Utilice la clase <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b4f7f-155">Use the <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> class.</span></span></p>
<p><span data-ttu-id="b4f7f-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> puede devolver datos para equipos que tengan tanto direcciones IPv4 como direcciones IPv6.</span><span class="sxs-lookup"><span data-stu-id="b4f7f-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> can return data for computers that have both IPv4 addresses and IPv6 addresses.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-157">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colPings = objWMIService.ExecQuery _
    (&quot;Select * From Win32_PingStatus where Address = &#39;192.168.1.1&#39;&quot;)

For Each objStatus in colPings
    If IsNull(objStatus.StatusCode) _
        or objStatus.StatusCode<>0 Then 
        WScript.Echo &quot;Computer did not respond.&quot; 
    Else
        Wscript.Echo &quot;Computer responded.&quot;
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f7f-158">VB</span><span class="sxs-lookup"><span data-stu-id="b4f7f-158">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;client1&quot;
Set objShell = CreateObject(&quot;WScript.Shell&quot;)
Set objScriptExec = objShell.Exec( _
    &quot;ping -n 2 -w 1000 &quot; & strComputer)
strPingResults = LCase(objScriptExec.StdOut.ReadAll)
If InStr(strPingResults, &quot;reply from&quot;) Then
    If InStr(strPingResults, &quot;destination net unreachable&quot;) Then
        WScript.Echo strComputer & &quot;did not respond to ping.&quot;
    Else
        WScript.Echo strComputer & &quot; responded to ping.&quot;
    End If 
Else
    WScript.Echo strComputer & &quot; did not respond to ping.&quot;
End If
  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b4f7f-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4f7f-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4f7f-160">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b4f7f-160">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="b4f7f-161">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="b4f7f-161">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="b4f7f-162">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="b4f7f-162">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

