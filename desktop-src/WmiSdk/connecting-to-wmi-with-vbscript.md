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
# <a name="connecting-to-wmi-with-vbscript"></a>Conectarse a WMI con VBScript

Los scripts de WMI pueden condensar muchos de los pasos necesarios en un programa de C++. Pueden conectarse a WMI, no solo a través de un objeto [**SWbemLocator**](swbemlocator.md) , sino también a través del moniker "winmgmts:". Un moniker es un nombre corto que ubica un espacio de nombres, una clase o una instancia en WMI. El nombre "winmgmts:" es el moniker de WMI que indica a Windows Script Host que use los objetos WMI, se conecta al espacio de nombres predeterminado y obtiene un objeto [**SWbemServices**](swbemservices.md) . Otra información de conexión, como un nivel de suplantación o una clase o instancia específica, aparece en la cadena que sigue al nombre del moniker. Puede usar monikers en llamadas que creen u obtengan objetos WMI. Para obtener más información, vea [crear una cadena de moniker](constructing-a-moniker-string.md).

En el procedimiento siguiente se describe cómo conectarse a WMI mediante **SWbemLocator**.

**Para conectarse a WMI mediante SWbemLocator**

1.  Recupere un objeto localizador con una llamada a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Inicie sesión en el espacio de nombres mediante una llamada al método [**ConnectServer**](swbemlocator-connectserver.md) .

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Si no especifica un equipo en la llamada a [**ConnectServer**](swbemlocator-connectserver.md), WMI se conectará al equipo local. Si no especifica un espacio de nombres, WMI se conecta al espacio de nombres especificado en la clave del registro.

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **scripting** \\ **default namespace**

    El espacio de nombres predeterminado es la \\ raíz \\ cimv2. Para obtener más información sobre los espacios de nombres, vea [Crear jerarquías en WMI](creating-hierarchies-within-wmi.md).

3.  Establezca el nivel de suplantación con una llamada al método [**SWbemServices. \_ Security**](swbemservices-security-.md) .

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

4.  Implemente el propósito del script.

    WMI expone una variedad de objetos de scripting que usan para tener acceso a los datos de la red y manipularlos. Para obtener más información, consulte [manipular la información de clase e instancia](manipulating-class-and-instance-information.md) y la [API de scripting para WMI](scripting-api-for-wmi.md).

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

    

En el procedimiento siguiente se describe cómo conectarse a WMI y recuperar un objeto con un moniker.

**Para conectarse a WMI y recuperar un objeto con un moniker**

1.  Llame a [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) con un moniker en el parámetro de entrada.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Moiniker contiene una serie de elementos que puede usar para conectarse a WMI:

    -   "Winmgmts:" indica a WSH que use los [objetos de API de scripting](scripting-api-objects.md). En este ejemplo concreto, WSH sabrá que debe devolver un SWbemObject que describa el primer scheduledJob Win32 del \_ sistema. Otros posibles objetos que se van a devolver serían un objeto SWbemCollection o [**SWbemServices**](swbemservices.md) , en función del moniker descrito.

    -   Opcionalmente, puede establecer los niveles de seguridad de la conexión. Sin embargo, tenga en cuenta que no puede establecer la información de nombre y contraseña en un moniker. Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).

    -   Opcionalmente, puede definir la ruta de acceso al objeto WMI. Esto incluye el equipo local o remoto, el espacio de nombres, así como el nombre de la clase. Para obtener más información acerca del uso de la expresión [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) de VBScript en scripts de WMI, vea [crear una instancia](creating-an-instance.md) y [recuperar una instancia de WMI](retrieving-an-instance.md).

2.  En lugar de recuperar un único elemento o colección, también puede optar por recuperar el objeto [**SWbemServices**](swbemservices.md) (como se describe en el ejemplo anterior). Después, puede llamar a consultas adicionales en el objeto devuelto.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    En el ejemplo anterior, Impersonate o impersonationLevel = 3 es el nivel de seguridad de proceso predeterminado. En el ejemplo siguiente, no es necesario especificar este nivel de seguridad del proceso a menos que necesite cambiar la seguridad del proceso a **Delegate**. Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
