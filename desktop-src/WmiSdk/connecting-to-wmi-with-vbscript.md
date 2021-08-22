---
description: Los scripts WMI pueden condensar muchos de los pasos necesarios en un programa de C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Conexión a WMI con VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b4e71f4225a55e24432562d4c35754080b9746386489b7dbf7061cb65c9771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131617"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Conexión a WMI con VBScript

Los scripts WMI pueden condensar muchos de los pasos necesarios en un programa de C++. Pueden conectarse a WMI, no solo a través de un objeto [**SWbemLocator,**](swbemlocator.md) sino también a través del moniker "winmgmts:". Un moniker es un nombre corto que busca un espacio de nombres, una clase o una instancia en WMI. El nombre "winmgmts:" es el moniker WMI que indica al host de script de Windows que use los objetos WMI, se conecta al espacio de nombres predeterminado y obtiene un objeto [**SWbemServices.**](swbemservices.md) Otra información de conexión, como un nivel de suplantación o una clase o instancia específica, aparece en la cadena que sigue al nombre del moniker. Puede usar monikers en llamadas que crean u obtienen objetos WMI. Para obtener más información, [vea Constructing a Moniker String](constructing-a-moniker-string.md).

En el procedimiento siguiente se describe cómo conectarse a WMI mediante **SWbemLocator**.

**Para conectarse a WMI mediante SWbemLocator**

1.  Recuperar un objeto de localizador con una llamada a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Inicie sesión en el espacio de nombres mediante una llamada al [**método ConnectServer.**](swbemlocator-connectserver.md)

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Si no especifica un equipo en la llamada a [**ConnectServer**](swbemlocator-connectserver.md), WMI se conecta al equipo local. Si no especifica un espacio de nombres, WMI se conecta al espacio de nombres especificado en la clave del Registro.

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Default Namespace**

    El espacio de nombres predeterminado \\ es \\ root cimv2. Para obtener más información sobre los espacios de nombres, vea [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).

3.  Establezca el nivel de suplantación con una llamada al [**método SWbemServices.Security. \_**](swbemservices-security-.md)

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

4.  Implemente el propósito del script.

    WMI expone una variedad de objetos de scripting que usan para acceder a los datos y manipularlos a través de la red. Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and Scripting API for [WMI](scripting-api-for-wmi.md).

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

    

En el procedimiento siguiente se describe cómo conectarse a WMI y recuperar un objeto mediante un moniker.

**Para conectarse a WMI y recuperar un objeto mediante un moniker**

1.  Llame [**a GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) con un moniker en el parámetro de entrada.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    El moiniker contiene una serie de elementos que puede usar para conectarse a WMI:

    -   "winmgmts:" indica a WSH que use objetos [de LA API de scripting.](scripting-api-objects.md) En este ejemplo concreto, WSH sabrá que debe devolver un objeto SWbemObject que describa el primer trabajo programado de Win32 \_ en el sistema. Otros objetos posibles que se devolverán serían un objeto SWbemCollection o [**SWbemServices,**](swbemservices.md) en función de lo que describa el moniker.

    -   Opcionalmente, puede establecer los niveles de seguridad de la conexión. Sin embargo, tenga en cuenta que no puede establecer la información de nombre y contraseña en un moniker. Para obtener más información, vea [Securing Scripting Clients](securing-scripting-clients.md).

    -   Opcionalmente, puede definir la ruta de acceso al objeto WMI. Esto incluye el equipo local o remoto, el espacio de nombres, así como el nombre de la clase . Para obtener más información sobre el uso de [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) de VBScript en scripts WMI, vea Crear una [instancia](creating-an-instance.md) y [Recuperar una instancia de WMI.](retrieving-an-instance.md)

2.  En lugar de recuperar un único elemento o colección, también puede elegir recuperar el objeto [**SWbemServices**](swbemservices.md) (como se describe en el ejemplo anterior). Después, puede llamar a consultas adicionales en el objeto devuelto.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    En el ejemplo anterior, suplantar o suplantarLevel=3 es el nivel de seguridad del proceso predeterminado. En el ejemplo siguiente, no es necesario especificar este nivel de seguridad de proceso a menos que tenga que cambiar la seguridad del proceso para **delegar**. Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
