---
description: Puede ver o manipular cualquier información disponible a través de WMI mediante scripts.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Creación de un script de WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003108"
---
# <a name="creating-a-wmi-script"></a>Creación de un script de WMI

Puede ver o manipular cualquier información disponible a través de WMI mediante scripts. Los scripts se pueden escribir en cualquier lenguaje de scripting que admita el hospedaje de scripts de Microsoft ActiveX, incluido Visual Basic Scripting Edition (VBScript), PowerShell y Perl. Windows Script Host (WSH), las páginas de Active Server e Internet Explorer pueden hospedar todos los scripts de WMI.

> [!Note]
>
> El lenguaje de scripting principal que actualmente admite WMI es PowerShell. Sin embargo, WMI también contiene un cuerpo sólido de compatibilidad con scripting para VBScript y otros lenguajes que tienen acceso a la [API de scripting para WMI](scripting-api-for-wmi.md).

 

## <a name="wmi-scripting-languages"></a>Lenguajes de scripting de WMI

Los dos idiomas principales admitidos por WMI son PowerShell y VBScript (a través de Windows Script Host o WSH).

-   **PowerShell** se diseñó con la estrecha integración con WMI en mente. Como tal, gran parte de los elementos subyacentes de WMI se integran en los cmdlets de WMI: [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)y [Remove-WMIObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1). En la tabla siguiente se describen los procesos generales que se usan para obtener acceso a la información de WMI. Tenga en cuenta que, aunque la mayoría de estos ejemplos usan Get-WMIObject, muchos de los cmdlets de WMI de PowerShell tienen los mismos parámetros, como *-Class* o *-Credentials*. Por lo tanto, muchos de estos procesos también funcionan para otros objetos. Para obtener una explicación más detallada de PowerShell y WMI, consulte [usar el Cmdlet Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) y [Windows PowerShell-la conexión WMI](/previous-versions/technet-magazine/cc162365(v=msdn.10)).

-   En cambio, **VBScript** realiza llamadas explícitamente a la [API de scripting para WMI](scripting-api-for-wmi.md), tal y como se mencionó anteriormente. Otros lenguajes, como Perl, también pueden usar la API de scripting para WMI. Sin embargo, para los fines de esta documentación, la mayoría de los ejemplos que muestran la API de scripting para WMI usarán VBScript. Sin embargo, cuando una técnica de programación es específica de VBScript, se le llamará.

    VBScript esencialmente tiene dos maneras independientes de obtener acceso a WMI. El primero es el uso de un objeto [**SWbemLocator**](swbemlocator.md) para conectarse a WMI. Como alternativa, puede usar [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) y un moniker. Un moniker es una cadena que puede describir un número de elementos: las credenciales, la configuración de suplantación, el equipo al que desea conectarse, el [*espacio de nombres*](gloss-n.md) de WMI (es decir, la ubicación general donde WMI almacena los grupos de objetos) y el objeto WMI que desea recuperar. Muchos de los ejemplos siguientes describen ambas técnicas. Para obtener más información, vea [construir una cadena de moniker](constructing-a-moniker-string.md) y [describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

    Independientemente de la técnica que utilice para conectarse a WMI, es probable que recupere uno o más objetos de la API de scripting. El más común es [**SWbemObject**](swbemobject.md), que WMI usa para describir un objeto WMI. Como alternativa, puede usar un objeto [**SWbemServices**](swbemservices.md) para describir el propio servicio WMI o un objeto [**SWbemObjectPath**](swbemobjectpath.md) para describir la ubicación de un objeto WMI. Para obtener más información, vea [scripting con](scripting-with-swbemobject.md) [objetos auxiliares de scripting](scripting-helper-objects.md)y SWbemObject.

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>Usar WMI y un lenguaje de scripting, cómo...

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... ¿conectarse a WMI?
</dt> <dd>

Para VBScript y la API de scripting para WMI, recupere un objeto [**SWbemServices**](swbemservices.md) con un moniker y una llamada a [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)). Como alternativa, puede conectarse al servidor con una llamada a [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). A continuación, puede utilizar el objeto para tener acceso a un espacio de nombres WMI específico o a una instancia de clase WMI.

Para PowerShell, la conexión a WMI normalmente se realiza directamente en la llamada de cmdlet; como tal, no es necesario realizar ningún paso adicional.

Para obtener más información, vea [describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md), [construir una cadena de moniker](constructing-a-moniker-string.md)y [conectarse a WMI con VBScript](connecting-to-wmi-with-vbscript.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... ¿recuperar información de WMI?
</dt> <dd>

Para VBScript y la API de scripting para WMI, use una función de recuperación, como [**WbemServices. Get**](swbemservices-get.md) o [**WbemServices. instances**](swbemservices-instancesof.md). También puede colocar el nombre de clase del objeto que se va a recuperar en un moniker, que puede ser más eficaz.

Para PowerShell, use el parámetro *-Class* . Tenga en cuenta que-Class es el parámetro predeterminado; como tal, no es necesario que lo indique explícitamente.

Para obtener más información, consulte [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... ¿crear una consulta WMI?
</dt> <dd>

Para VBScript y la API de scripting para WMI, use el método [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .

Para PowerShell, use el parámetro *-query* . También puede filtrar mediante el parámetro *-Filter* .

Para obtener más información, consulte [consultar WMI](querying-wmi.md).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... ¿enumerar a través de una lista de objetos WMI?
</dt> <dd>

Para VBScript y la API de scripting para WMI, use el objeto contenedor [**SWbemObjectSet**](swbemobjectset.md) , que se trata en el script como una colección que se puede enumerar. Puede recuperar un **SWbemObjectSet** de una llamada desde [**SWbemServices. instances**](swbemservices-instancesof.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md).

PowerShell puede recuperar y controlar las enumeraciones como lo haría con cualquier otro objeto. no hay nada particularmente único en WMI.

Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... ¿tiene acceso a un espacio de nombres WMI diferente?
</dt> <dd>

Para VBScript y la API de scripting para WMI, establezca el espacio de nombres en el moniker o, de lo contrario, puede indicar explícitamente el espacio de nombres en la llamada a [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

Para PowerShell, use el parámetro *-namespace* . El espacio de nombres predeterminado es "root \\ cimV2"; sin embargo, muchas clases anteriores se almacenan en "root \\ default".

Para buscar la ubicación de una clase WMI determinada, examine la página de referencia. Como alternativa, puede explorar manualmente un espacio de nombres mediante Get-WmiObject.


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... ¿recuperar todas las instancias secundarias de una clase?
</dt> <dd>

Para los lenguajes que usan directamente la API de scripting para WMI y PowerShell, WMI admite la recuperación de las clases secundarias de una clase base. Por lo tanto, para recuperar las instancias secundarias, solo necesita buscar la clase primaria. En el siguiente ejemplo se busca [**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), que es una clase WMI preinstalada que representa discos lógicos en un sistema de equipo basado en Windows. Como tal, la búsqueda de esta clase primaria también devuelve instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), que es lo que usa Windows para describir las unidades de disco duro. Para obtener más información, vea [modelo de información común](common-information-model.md). WMI proporciona un esquema completo de estas clases preinstaladas que le permiten tener acceso a objetos administrados y controlarlos. Para obtener más información, vea [clases Win32](/windows/desktop/CIMWin32Prov/win32-provider) y [clases WMI](wmi-classes.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... ¿buscar un objeto WMI?
</dt> <dd>

En el caso de la API de scripting para WMI y PowerShell, WMI utiliza una combinación de espacio de nombres, nombre de clase y propiedades de clave para identificar de forma única una instancia de WMI determinada. En conjunto, esto se conoce como la ruta de acceso del objeto WMI. En el caso de VBScript, la propiedad [**SWbemObject. Path \_**](swbemobject-path-.md) describe la ruta de acceso de cualquier objeto dado devuelto por la API de scripting. Para PowerShell, cada objeto WMI tendrá una \_ \_ propiedad path. Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md) .

Además del espacio de nombres y el nombre de clase, un objeto WMI también tendrá una propiedad clave que identifica de forma única esa instancia en comparación con otras instancias de su equipo. Por ejemplo, la propiedad **DeviceID** es la propiedad clave de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Para obtener más información, consulte [Managed Object Format (MOF)](managed-object-format--mof-.md).

Por último, la ruta de acceso relativa es simplemente una forma abreviada de la ruta de acceso e incluye el nombre de la clase y el valor de la clave. En los ejemplos siguientes, la ruta de acceso puede ser " \\ \\ computerName \\ root \\ cimv2: Win32 \_ LogicalDisk. DeviceID =" d: "", mientras que la ruta de acceso relativa sería "" Win32LogicalDisk. DeviceID = "d" "".


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... ¿establecer información en WMI?
</dt> <dd>

Para VBScript y la API de scripting para WMI, use el método [**SWbemObject \_ . put**](swbemobject-put-.md) .

En el caso de PowerShell, puede usar el método put, o bien [set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

Para obtener más información, vea [modificar una propiedad de instancia](modifying-an-instance-property.md).


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... ¿usar credenciales diferentes?
</dt> <dd>

En el caso de VBScript y la API de scripting para WMI, use los parámetros de *nombre de usuario* y *contraseña* en el método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

Para PowerShell, use el parámetro *-Credential* .

Tenga en cuenta que solo puede usar credenciales alternativas en un sistema remoto. Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... ¿tiene acceso a un equipo remoto?
</dt> <dd>

En el caso de VBScript y la API de scripting para WMI, indique explícitamente el nombre del equipo en el moniker, o bien en la llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Para obtener más información, vea [conectarse a WMI de forma remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md).

Para PowerShell, use el parámetro *-ComputerName* . Para obtener más información, consulte [conexión a WMI de forma remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... ¿establecer los niveles de autenticación y suplantación?
</dt> <dd>

Para VBScript y la API de scripting para WMI, use la propiedad [**SWbemServices \_ . Security**](swbemlocator-security-.md) en el objeto de servidor devuelto, o bien establezca los valores relevantes en el moniker.

Para PowerShell, use los parámetros *-Authentication* y *-Impersonation* , respectivamente. Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).

Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... ¿controlar los errores en WMI?
</dt> <dd>

En el caso de la API de scripting para WMI, el proveedor puede proporcionar un objeto [**SWbemLastError**](swbemlasterror.md) para proporcionar más información sobre un error.

En VBScript, en concreto, el control de errores también se admite mediante el objeto **Err** nativo. También puede tener acceso al objeto [**SWbemLastError**](swbemlasterror.md), tal y como se ha descrito anteriormente. Para obtener más información, vea [recuperar un código de error](retrieving-an-error-code.md).

Para PowerShell, puede usar las técnicas estándar de control de errores de PowerShell. Para obtener más información, vea [Introducción al control de errores en PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
